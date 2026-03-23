# How to Use x402 Proxy

## Base URL

```
https://x402.nodit.io
```

## Overview

The x402 proxy provides two billing modes for accessing Nodit APIs using USDC payments instead of API keys.

| Mode       | Auth       | Payment                                      | Best For                            |
|------------|------------|----------------------------------------------|-------------------------------------|
| **Credit** | SIWX → JWT | Pre-charge USDC → off-chain credit deduction | Repeated usage, lower per-call cost |
| **PPU**    | None       | Per-request on-chain USDC settlement         | One-off calls, no signup needed     |

## Endpoints

### Authentication

| Method | Path    | Auth | Description                            |
|--------|---------|------|----------------------------------------|
| POST   | `/auth` | None | SIWX sign-in (SIWE/SIWS) → returns JWT |

### Credit Management

| Method | Path                   | Auth | Description                 |
|--------|------------------------|------|-----------------------------|
| GET    | `/credit/balance`      | JWT  | Check credit balance        |
| POST   | `/credit/charge`       | JWT  | Charge USDC → credits       |
| GET    | `/credit/transactions` | JWT  | Credit charge/spend history |

### API Proxy (Credit Mode)

| Method | Path                                                    | Auth | Description                        |
|--------|---------------------------------------------------------|------|------------------------------------|
| POST   | `/credit/v1/{chain}/{network}/{category}/{operationId}` | JWT  | Data API (credit billing)          |
| POST   | `/credit/{chain}/{network}/json-rpc`                    | JWT  | Node API JSON-RPC (credit billing) |

### API Proxy (PPU Mode)

| Method | Path                                                         | Auth | Description                             |
|--------|--------------------------------------------------------------|------|-----------------------------------------|
| POST   | `/pay-per-use/v1/{chain}/{network}/{category}/{operationId}` | None | Data API (per-request payment)          |
| POST   | `/pay-per-use/{chain}/{network}/json-rpc`                    | None | Node API JSON-RPC (per-request payment) |

### Utility

| Method | Path           | Auth | Description                               |
|--------|----------------|------|-------------------------------------------|
| GET    | `/healthcheck` | None | Health check (MySQL + Redis connectivity) |

---

## URL Patterns

| Mode   | API Type | URL Pattern                                                  |
|--------|----------|--------------------------------------------------------------|
| Credit | Data API | `/credit/v1/{chain}/{network}/{category}/{operationId}`      |
| Credit | Node API | `/credit/{chain}/{network}/json-rpc`                         |
| PPU    | Data API | `/pay-per-use/v1/{chain}/{network}/{category}/{operationId}` |
| PPU    | Node API | `/pay-per-use/{chain}/{network}/json-rpc`                    |

---

## 402 Response Structure

Requesting an API without payment returns a 402. The payment requirements are base64-encoded in the `Payment-Required` response header. Decode it to select the desired network from the `accepts` array.

```ts
// Base64-decode from Payment-Required header
const paymentRequired = JSON.parse(
  Buffer.from(res402.headers['payment-required'], 'base64').toString()
);
const accept = paymentRequired.accepts.find((a: any) => a.network === 'eip155:8453');
```

Decoded JSON structure:

```json
{
  "x402Version": 2,
  "accepts": [
    {
      "network": "eip155:8453",
      "asset": "0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913",
      "payTo": "0xeD2adE260ed6F852DB9145D7A3483dE051908672",
      "amount": "1000",
      "maxTimeoutSeconds": 3600,
      "scheme": "exact",
      "extra": { "name": "USDC", "version": "2" }
    },
    {
      "network": "solana:5eykt4UsFv8P8NJdTREpY1vzqKqZKvdp",
      "asset": "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v",
      "payTo": "2LWbc9Mi6dRUrdEHBttoNS4udDtH1A4xwBdm1EKqcT57",
      "amount": "1000",
      "scheme": "exact",
      "extra": { "name": "USDC", "version": "1", "feePayer": "GVJJ7rdGiXr5xaYbRwRbjfaJL7fmwRygFi1H6aGqDveb" }
    }
  ]
}
```

### payment-signature Structure (JSON → base64)

**EVM:**
```json
{
  "x402Version": 2,
  "resource": { "url": "<api-url>", "description": "...", "mimeType": "application/json" },
  "accepted": { "network": "...", "asset": "...", "payTo": "...", "amount": "...", "..." : "..." },
  "payload": {
    "signature": "0x...",
    "authorization": {
      "from": "0x_wallet", "to": "0x_payTo", "value": "1000",
      "validAfter": "0", "validBefore": "1741234567", "nonce": "0x..."
    }
  }
}
```

**Solana:**
```json
{
  "x402Version": 2,
  "resource": { "url": "<api-url>", "description": "...", "mimeType": "application/json" },
  "accepted": { "network": "...", "asset": "...", "payTo": "...", "amount": "...", "..." : "..." },
  "payload": {
    "transaction": "<base64-encoded-versioned-transaction>"
  }
}
```

---

## Key Business Rules

| Item              | Value                       |
|-------------------|-----------------------------|
| Credit unit       | 1 Credit = $0.000001 USDC   |
| Min charge        | 1,000,000 credits ($1 USDC) |
| Charge rate limit | 10 per minute per account   |
| JWT expiry        | 1 hour                      |
| PPU nonce TTL     | 300 seconds                 |
| Payment timeout   | 5 minutes (verifying state) |
| Settlement speed  | ~200ms (Base L2 / Solana)   |
| PPU min amount    | 0.001 USDC                  |

## Key Differences

|                          | Credit                    | PPU           |
|--------------------------|---------------------------|---------------|
| JWT Auth                 | Required (SIWx → `/auth`) | Not required  |
| Payment Timing           | Once at charge time       | Per request   |
| Minimum Payment          | 0.001 USDC                | 0.001 USDC    |
| payment-signature Header | Only when charging        | Every request |
