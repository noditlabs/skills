# PPU (Pay-Per-Use) Mode — Implementation Guide

> Before reading this document, review the endpoints, URL patterns, and 402 response structure in `how-to-use.md`.

## Flow Overview

No JWT required. USDC payment per request.

```
Step 1. API call (without auth)  → 402 response
Step 2. Decode Payment-Required header → select accept → generate payment-signature
Step 3. Re-request same API with payment-signature attached  → 200 + API response
```

---

## Step 1: API Call → Receive 402

Send a request without authentication to the per-operationId endpoint. See `how-to-use.md` Endpoints for URL patterns.

→ Returns a 402 response. Base64-decode the `Payment-Required` header to get the `accepts` array.

## Step 2: Generate payment-signature

Select a network from the `accepts` array. The signing method is the same as Credit Mode.

- **EVM**: EIP-3009 TransferWithAuthorization signature → see `credit-mode.md` Step 2-3 "EVM"
- **Solana**: USDC TransferChecked transaction build → see `credit-mode.md` Step 2-3 "Solana"

**payment-signature Payload Structure:**

```json
{
  "x402Version": 2,
  "resource": { "url": "<apiUrl>", "description": "Nodit API", "mimeType": "application/json" },
  "accepted": { /* entire selected accept object */ },
  "payload": {
    "signature": "<EIP-712 signature>",
    "authorization": { /* authorization object */ }
  }
}
```

For Solana, use `transaction` in `payload` instead of `signature`/`authorization`.

JSON → base64-encode and set as the `payment-signature` header.

## Step 3: Re-request

```
POST <same API URL>
Headers:
  Content-Type: application/json
  payment-signature: <base64 encoded paymentPayload>
Body: {same parameters}
```

→ 200 response + API result.

Unlike Credit Mode, no `Authorization` header is needed.

---

## PPU Pricing

`Max(cost, ppu_min_amount)` — ppu_min_amount = 0.001 USDC.

### Batch JSON-RPC (PPU)

Batch request price: `Max(sum(each method cost), max(each method ppu_min_amount))`
