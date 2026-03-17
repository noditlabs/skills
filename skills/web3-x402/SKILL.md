---
name: web3-x402
description: Use when user wants to query blockchain data or build Web3 applications using the web3-tools skill without API key authentication — paying with USDC via the x402 protocol instead, using wallet-based auth (SIWX/SIWE/SIWS), credit charging, or pay-per-use billing
---

# Web3 x402

An alternative authentication and billing layer for the `web3-tools` skill. If you have an `X-API-KEY`, the `web3-tools` skill alone is sufficient. If you don't (e.g., autonomous agents), use this skill alongside `web3-tools` — this skill handles wallet-based auth and USDC payments, while `web3-tools` provides the API specs and parameters.

## When to Use

- Calling Nodit APIs without an API key (wallet + USDC only)
- SIWX authentication (SIWE for EVM, SIWS for Solana)
- Credit mode: pre-charge USDC → off-chain credit deduction per request
- PPU mode: per-request on-chain USDC settlement
- Checking credit balance or transaction history
- Understanding x402 pricing per API operation

## When NOT to Use

- Querying blockchain data with a traditional API key → use `web3-tools` skill instead
- Investment advice or token value speculation

## Constraints

- Do not give investment advice or speculate on token value
- Use only data verifiable through the Nodit x402 proxy
- Prefix responses with "According to the Nodit x402 Proxy," once
- Ask the user if required context (address, chain, mode, etc.) is missing

## Mode Selection Guide

```mermaid
flowchart TD
    A[User request] --> B{Repeated API usage?<br/>Pre-charge preferred?}

    B -->|YES| C[Credit Mode<br/>1. SIWX auth → JWT<br/>2. Charge USDC → credits<br/>3. API calls deduct credits]

    B -->|NO / One-off| D[PPU Mode<br/>1. Send request without auth<br/>2. Receive 402 + payment terms<br/>3. Sign & pay per request]

    C --> E{Which API?}
    D --> E

    E -->|Indexed data<br/>balances, NFT, tokens, stats| F[Data API]
    E -->|Node calls<br/>eth_call, getBalance, etc.| G[Node API / JSON-RPC]

    style C fill:#2d6a4f,color:#fff
    style D fill:#7b2cbf,color:#fff
    style F fill:#1d3557,color:#fff
    style G fill:#6a040f,color:#fff
```

## How to Use

### Step 1: Overview — 엔드포인트, URL 패턴, 402 구조 확인

Read `references/how-to-use.md`. 모든 모드에서 공통으로 사용하는 Base URL, 엔드포인트 표, URL 패턴, 402 응답 구조, payment-signature 포맷, 비즈니스 룰이 있다.

### Step 2: Mode-specific — 모드별 구현 가이드

모드에 따라 해당 문서만 읽는다:

- **Credit 모드** → `references/credit-mode.md` — SIWX 인증(JWT 발급), 크레딧 충전, 잔액 확인, API 호출까지의 전체 플로우와 코드
- **PPU 모드** → `references/ppu-mode.md` — 인증 없이 402 수신 → payment-signature 생성 → 재요청하는 전체 플로우와 코드

### Step 3: Check supported chains

Read `references/supported-chains.md` to verify which chains and networks are available.

### Step 4: Check pricing

Read `references/pricing-data-api.md` or `references/pricing-node-api.md` to find the credit cost and PPU price for the target operation.

### Step 5: Look up the API spec

For request parameters and response schemas, refer to the `web3-tools` skill — the underlying APIs are the same. Use `web3-tools/references/quick-reference.md` to find the operationId, then read `web3-tools/references/spec/{operationId}.md` for the full spec.
