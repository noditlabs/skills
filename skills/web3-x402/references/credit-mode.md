# Credit Mode — Implementation Guide

> Before reading this document, review the endpoints, URL patterns, and 402 response structure in `how-to-use.md`.

## Flow Overview

```
Step 1. Issue JWT       POST /auth                                           → accessToken
Step 2. Charge credits  POST /credit/charge                                  → 402 → re-request with payment-signature → charge complete
Step 3. Check balance   GET  /credit/balance                                 → { balance }
Step 4. API call        Request with JWT in Authorization header             → credits deducted
```

---

## Step 1: SIWX Authentication → JWT

Sign a message with your private key, then obtain a JWT via `POST /auth`. The JWT is valid for 24 hours.

### SIWE Message Format (EVM)

Follow the format below exactly. Each line is joined with `\n`.

```
x402.nodit.io wants you to sign in with your Ethereum account:
{walletAddress}

Sign in to x402.nodit.io

URI: https://x402.nodit.io
Version: 1
Chain ID: {chainId}
Nonce: {random hex 16bytes}
Issued At: {ISO 8601}
Expiration Time: {ISO 8601, +10 min recommended}
```

- Signature: `wallet.signMessage(message)` (EIP-191 personal_sign)
- `chainId`: The Chain ID of the user's selected network (e.g., Base Mainnet → `8453`)

### SIWS Message Format (Solana)

```
x402.nodit.io wants you to sign in with your Solana account:
{walletAddress}

Sign in to x402.nodit.io

URI: https://x402.nodit.io
Version: 1
Chain ID: {chainId}
Nonce: {random hex 16bytes}
Issued At: {ISO 8601}
Expiration Time: {ISO 8601, +10 min recommended}
```

- Signature: `nacl.sign.detached(messageBytes, secretKey)` → base58 encode
- `chainId`: The Chain ID of the user's selected network (e.g., Solana Mainnet → `5eykt4UsFv8P8NJdTREpY1vzqKqZKvdp`)

### POST /auth Request

```json
{
  "message": "<message string constructed above>",
  "signature": "<signature value>"
}
```

Response: `{ "accessToken": "<JWT>" }`

---

## Step 2: Charge Credits

### 2-1. Charge Request

```
POST /credit/charge
Headers: Authorization: Bearer <JWT>
Body: { "amount": "1000000" }   ← 1 USDC = 1,000,000 atomic units
```

→ Returns a 402 response. Base64-decode the `Payment-Required` header to get the `accepts` array.

### 2-2. Select an accept

Filter the `accepts` array by the `network` field to select the accept object for the user's desired payment network. See `supported-chains.md` for supported payment networks.

### 2-3. Generate payment-signature

The signing method differs depending on the selected network.

#### EVM: EIP-3009 TransferWithAuthorization Signature

EIP-712 typed data signature. Construct the domain and authorization objects.

**EIP-712 Domain:**

```json
{
  "name": "{accept.extra.name}",
  "version": "{accept.extra.version}",
  "chainId": "{chainId from accept.network}",
  "verifyingContract": "{accept.asset}"
}
```

**Authorization Object:**

```json
{
  "from": "{walletAddress}",
  "to": "{accept.payTo}",
  "value": "{accept.amount}",
  "validAfter": "0",
  "validBefore": "{current unix timestamp + accept.maxTimeoutSeconds (default 3600)}",
  "nonce": "{random 32bytes hex}"
}
```

**EIP-3009 Type Definition:**

```
TransferWithAuthorization(address from, address to, uint256 value, uint256 validAfter, uint256 validBefore, bytes32 nonce)
```

Signature: `wallet.signTypedData(domain, types, authorization)`

#### Solana: USDC TransferChecked Transaction

Build a VersionedTransaction (V0) and have only the user partial-sign it.

**Transaction Structure:**

| Field | Value |
|-------|-------|
| payerKey | `accept.extra.feePayer` (facilitator covers the fee) |
| recentBlockhash | Fetch from the target chain's RPC |

**Instruction Order (must be followed exactly):**

1. `ComputeBudgetProgram.setComputeUnitLimit({ units: 20000 })`
2. `ComputeBudgetProgram.setComputeUnitPrice({ microLamports: 1 })`
3. SPL Token `TransferChecked` instruction

**TransferChecked Instruction:**

| Field | Value |
|------|-----|
| programId | `TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA` |
| discriminator | `12` |
| amount | `accept.amount` (uint64 LE) |
| decimals | `6` (USDC) |

**Account Keys (order matters):**

1. source ATA (from, writable)
2. mint (`accept.asset`, readonly)
3. destination ATA (ATA of `accept.payTo`, writable)
4. authority (wallet pubkey, signer)

**ATA Address Derivation:**

`findProgramAddressSync([ownerPubkey, tokenProgram, mintPubkey], ATA_PROGRAM)`

- ATA Program: `ATokenGPvbdGVxr1b2hvZbsiqW5xWH25efTNsLJA8knL`

**Signing:** Only the user signs. The feePayer (facilitator) signs on the server side.

**Result:** Base64-encode the serialized transaction.

### 2-4. Construct the payment-signature Header

Wrap the signature result in the JSON below, base64-encode it, and set it as the `payment-signature` header.

**EVM:**

```json
{
  "x402Version": 2,
  "resource": { "url": "<chargeUrl>", "description": "Credit charge", "mimeType": "application/json" },
  "accepted": { /* entire selected accept object */ },
  "payload": {
    "signature": "<EIP-712 signature>",
    "authorization": { /* authorization object above */ }
  }
}
```

**Solana:**

```json
{
  "x402Version": 2,
  "resource": { "url": "<chargeUrl>", "description": "Credit charge", "mimeType": "application/json" },
  "accepted": { /* entire selected accept object */ },
  "payload": {
    "transaction": "<base64 encoded VersionedTransaction>"
  }
}
```

### 2-5. Re-request

```
POST /credit/charge
Headers:
  Authorization: Bearer <JWT>
  payment-signature: <base64 encoded paymentPayload>
Body: { "amount": "1000000" }
```

Response: `{ "balance": 1000000, "paymentResponse": { "txHash": "...", ... } }`

---

## Step 3: Check Balance

```
GET /credit/balance
Headers: Authorization: Bearer <JWT>
```

Response: `{ "balance": <number> }`

---

## Step 4: API Calls

If the credit balance is sufficient, credits are deducted and the API response is returned. If the balance is insufficient, a 402 is returned — attach a payment-signature to charge inline.

Send requests to the per-operationId endpoint with the JWT in the `Authorization: Bearer <JWT>` header. See `how-to-use.md` Endpoints for URL patterns.

Insufficient balance returns a 402 — attach a payment-signature to charge inline.

---

## Credit Charging Rates

| Payment Network | Chain ID                                | 1 USDC →          |
|-----------------|-----------------------------------------|-------------------|
| Base Mainnet    | eip155:8453                             | 1,000,000 credits |
| Base Sepolia    | eip155:84532                            | 100,000 credits   |
| Solana Mainnet  | solana:5eykt4UsFv8P8NJdTREpY1vzqKqZKvdp | 1,000,000 credits |
| Solana Devnet   | solana:EtWTRABZaYq6iMfeYKouRu166VU2xqa1 | 100,000 credits   |
