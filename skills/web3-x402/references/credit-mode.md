# Credit Mode — Implementation Guide

> 이 문서를 읽기 전에 `how-to-use.md`의 엔드포인트, URL 패턴, 402 응답 구조를 먼저 확인하라.

## Flow Overview

```
Step 1. JWT 발급       POST /auth                                           → accessToken
Step 2. 크레딧 충전     POST /credit/charge                                  → 402 → payment-signature 첨부 재요청 → 충전 완료
Step 3. 잔액 확인       GET  /credit/balance                                 → { balance }
Step 4. API 호출       JWT를 Authorization 헤더에 넣어 요청                   → 크레딧 차감
```

---

## Step 1: SIWX Authentication → JWT

Private key로 메시지에 서명한 뒤 `POST /auth`로 JWT를 발급받는다. JWT는 24시간 유효.

### SIWE 메시지 구성 (EVM)

아래 형식을 정확히 따라야 한다. 각 줄은 `\n`으로 연결한다.

```
x402.nodit-stg.net wants you to sign in with your Ethereum account:
{walletAddress}

Sign in to x402.nodit-stg.net

URI: https://x402.nodit-stg.net
Version: 1
Chain ID: {chainId}
Nonce: {random hex 16bytes}
Issued At: {ISO 8601}
Expiration Time: {ISO 8601, +10분 권장}
```

- 서명: `wallet.signMessage(message)` (EIP-191 personal_sign)
- `chainId`: 유저가 선택한 네트워크의 Chain ID (예: Base Mainnet → `8453`)

### SIWS 메시지 구성 (Solana)

```
x402.nodit-stg.net wants you to sign in with your Solana account:
{walletAddress}

Sign in to x402.nodit-stg.net

URI: https://x402.nodit-stg.net
Version: 1
Chain ID: {chainId}
Nonce: {random hex 16bytes}
Issued At: {ISO 8601}
Expiration Time: {ISO 8601, +10분 권장}
```

- 서명: `nacl.sign.detached(messageBytes, secretKey)` → base58 인코딩
- `chainId`: 유저가 선택한 네트워크의 Chain ID (예: Solana Mainnet → `5eykt4UsFv8P8NJdTREpY1vzqKqZKvdp`)

### POST /auth 요청

```json
{
  "message": "<위에서 구성한 메시지 문자열>",
  "signature": "<서명 값>"
}
```

응답: `{ "accessToken": "<JWT>" }`

---

## Step 2: Charge Credits

### 2-1. 충전 요청

```
POST /credit/charge
Headers: Authorization: Bearer <JWT>
Body: { "amount": "1000000" }   ← 1 USDC = 1,000,000 atomic units
```

→ 402 응답. `Payment-Required` 헤더를 base64 디코딩하여 `accepts` 배열을 얻는다.

### 2-2. accept 선택

`accepts` 배열에서 유저가 결제에 사용할 네트워크의 accept 객체를 `network` 필드로 필터링하여 선택한다. 지원되는 결제 네트워크는 `supported-chains.md` 참조.

### 2-3. payment-signature 생성

선택한 네트워크에 따라 서명 방식이 다르다.

#### EVM: EIP-3009 TransferWithAuthorization 서명

EIP-712 typed data 서명. domain과 authorization 객체를 구성한다.

**EIP-712 Domain:**

```json
{
  "name": "{accept.extra.name}",
  "version": "{accept.extra.version}",
  "chainId": "{accept.network의 chainId}",
  "verifyingContract": "{accept.asset}"
}
```

**Authorization 객체:**

```json
{
  "from": "{walletAddress}",
  "to": "{accept.payTo}",
  "value": "{accept.amount}",
  "validAfter": "0",
  "validBefore": "{현재 unix timestamp + accept.maxTimeoutSeconds (기본 3600)}",
  "nonce": "{random 32bytes hex}"
}
```

**EIP-3009 Type 정의:**

```
TransferWithAuthorization(address from, address to, uint256 value, uint256 validAfter, uint256 validBefore, bytes32 nonce)
```

서명: `wallet.signTypedData(domain, types, authorization)`

#### Solana: USDC TransferChecked 트랜잭션

VersionedTransaction (V0)을 빌드하고 유저만 partial sign한다.

**트랜잭션 구성:**

| 항목 | 값 |
|------|-----|
| payerKey | `accept.extra.feePayer` (facilitator가 수수료 부담) |
| recentBlockhash | 해당 체인의 RPC에서 조회 |

**Instruction 순서 (반드시 지켜야 함):**

1. `ComputeBudgetProgram.setComputeUnitLimit({ units: 20000 })`
2. `ComputeBudgetProgram.setComputeUnitPrice({ microLamports: 1 })`
3. SPL Token `TransferChecked` instruction

**TransferChecked instruction:**

| 항목 | 값 |
|------|-----|
| programId | `TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA` |
| discriminator | `12` |
| amount | `accept.amount` (uint64 LE) |
| decimals | `6` (USDC) |

**Account keys (순서 중요):**

1. source ATA (from, writable)
2. mint (`accept.asset`, readonly)
3. destination ATA (`accept.payTo`의 ATA, writable)
4. authority (wallet pubkey, signer)

**ATA 주소 계산:**

`findProgramAddressSync([ownerPubkey, tokenProgram, mintPubkey], ATA_PROGRAM)`

- ATA Program: `ATokenGPvbdGVxr1b2hvZbsiqW5xWH25efTNsLJA8knL`

**서명:** 유저만 sign. feePayer(facilitator)는 서버에서 서명한다.

**결과:** 직렬화한 트랜잭션을 base64 인코딩.

### 2-4. payment-signature 헤더 구성

서명 결과를 아래 JSON으로 감싸고 base64 인코딩하여 `payment-signature` 헤더에 넣는다.

**EVM:**

```json
{
  "x402Version": 2,
  "resource": { "url": "<chargeUrl>", "description": "Credit charge", "mimeType": "application/json" },
  "accepted": { /* 선택한 accept 객체 전체 */ },
  "payload": {
    "signature": "<EIP-712 서명>",
    "authorization": { /* 위의 authorization 객체 */ }
  }
}
```

**Solana:**

```json
{
  "x402Version": 2,
  "resource": { "url": "<chargeUrl>", "description": "Credit charge", "mimeType": "application/json" },
  "accepted": { /* 선택한 accept 객체 전체 */ },
  "payload": {
    "transaction": "<base64 encoded VersionedTransaction>"
  }
}
```

### 2-5. 재요청

```
POST /credit/charge
Headers:
  Authorization: Bearer <JWT>
  payment-signature: <base64 encoded paymentPayload>
Body: { "amount": "1000000" }
```

응답: `{ "balance": 1000000, "paymentResponse": { "txHash": "...", ... } }`

---

## Step 3: Check Balance

```
GET /credit/balance
Headers: Authorization: Bearer <JWT>
```

응답: `{ "balance": <number> }`

---

## Step 4: API Calls

크레딧 잔액이 충분하면 크레딧이 차감되고 API 응답을 받는다. 잔액이 부족하면 402가 반환되며, payment-signature를 첨부하여 인라인 충전할 수 있다.

operationId별 endpoint에 JWT를 `Authorization: Bearer <JWT>` 헤더로 첨부하여 요청한다. URL 패턴은 `how-to-use.md`의 Endpoints 참조.

잔액 부족 시 402 응답 — payment-signature를 첨부하면 인라인 충전 가능.

---

## Credit Charging Rates

| Payment Network | Chain ID                                | 1 USDC →          |
|-----------------|-----------------------------------------|-------------------|
| Base Mainnet    | eip155:8453                             | 1,000,000 credits |
| Base Sepolia    | eip155:84532                            | 100,000 credits   |
| Solana Mainnet  | solana:5eykt4UsFv8P8NJdTREpY1vzqKqZKvdp | 1,000,000 credits |
| Solana Devnet   | solana:EtWTRABZaYq6iMfeYKouRu166VU2xqa1 | 100,000 credits   |
