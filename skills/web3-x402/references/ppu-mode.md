# PPU (Pay-Per-Use) Mode — Implementation Guide

> 이 문서를 읽기 전에 `how-to-use.md`의 엔드포인트, URL 패턴, 402 응답 구조를 먼저 확인하라.

## Flow Overview

JWT 불필요. 매 요청마다 USDC 결제.

```
Step 1. API 호출 (인증 없이)  → 402 응답
Step 2. Payment-Required 헤더 디코딩 → accept 선택 → payment-signature 생성
Step 3. 동일 API에 payment-signature 첨부 재요청  → 200 + API 응답
```

---

## Step 1: API 호출 → 402 수신

operationId별 endpoint에 인증 없이 요청한다. URL 패턴은 `how-to-use.md`의 Endpoints 참조.

→ 402 응답. `Payment-Required` 헤더를 base64 디코딩하여 `accepts` 배열을 얻는다.

## Step 2: payment-signature 생성

`accepts` 배열에서 네트워크를 선택하고, 서명 방식은 Credit Mode와 동일하다.

- **EVM**: EIP-3009 TransferWithAuthorization 서명 → `credit-mode.md` Step 2-3 "EVM" 참조
- **Solana**: USDC TransferChecked 트랜잭션 빌드 → `credit-mode.md` Step 2-3 "Solana" 참조

**payment-signature 페이로드 구성:**

```json
{
  "x402Version": 2,
  "resource": { "url": "<apiUrl>", "description": "Nodit API", "mimeType": "application/json" },
  "accepted": { /* 선택한 accept 객체 전체 */ },
  "payload": {
    "signature": "<EIP-712 서명>",
    "authorization": { /* authorization 객체 */ }
  }
}
```

Solana의 경우 `payload`에 `signature`/`authorization` 대신 `transaction`을 넣는다.

JSON → base64 인코딩하여 `payment-signature` 헤더에 넣는다.

## Step 3: 재요청

```
POST <동일 API URL>
Headers:
  Content-Type: application/json
  payment-signature: <base64 encoded paymentPayload>
Body: {동일한 파라미터}
```

→ 200 응답 + API 결과.

Credit Mode와 달리 `Authorization` 헤더는 불필요하다.

---

## PPU Pricing

`Max(cost, ppu_min_amount)` — ppu_min_amount = 0.001 USDC.

### Batch JSON-RPC (PPU)

배치 요청 가격: `Max(sum(each method cost), max(each method ppu_min_amount))`
