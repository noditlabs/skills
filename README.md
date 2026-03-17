# Nodit Skills

[Nodit](https://nodit.io) blockchain API skills for AI coding agents. Query on-chain data across 30+ chains directly from your IDE.

## Installation

via [skills.sh](https://skills.sh):

```bash
npx skills add noditlabs/skills --yes
```

## Skills

### `web3-tools`

Nodit API를 활용한 멀티체인 블록체인 데이터 조회 스킬. API 키 기반 인증.

**Use when:**
- Token / NFT 잔액 및 메타데이터 조회
- 트랜잭션 조회 및 히스토리 분석
- 블록 데이터 조회
- 스마트 컨트랙트 상태 읽기 (eth_call)
- ENS 이름 해석
- 온체인 이벤트 모니터링 (Webhook)
- 가스비 추정 및 조회
- 토큰 홀더 / 전송 내역 분석

**Supported APIs:**

| API Type | Description | Format |
|----------|-------------|--------|
| Data API | 인덱싱된 블록체인 데이터 조회 (잔액, NFT, 토큰, 통계 등) | REST |
| Node API | 블록체인 노드 직접 호출 (JSON-RPC) | JSON-RPC |
| Aptos Indexer API | Aptos 인덱싱 데이터 조회 | GraphQL |
| Webhook API | 온체인 이벤트 구독 관리 | REST |

**Supported Chains:**

Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc, Chiliz, Ethereum Classic, Solana, Sui, Aptos, Bitcoin, Bitcoin Cash, Dogecoin, Tron, XRPL

---

### `web3-x402`

API 키 없이 USDC 결제로 Nodit API에 접근하는 스킬. [x402 프로토콜](https://www.x402.org/) 기반.

`web3-tools` 스킬과 함께 사용되며, 이 스킬은 인증과 결제를 담당하고 API 스펙은 `web3-tools`를 참조합니다.

**Use when:**
- API 키 없이 블록체인 데이터를 조회하고 싶을 때
- 자율 에이전트가 지갑 기반으로 API를 호출할 때
- SIWX 인증 (SIWE for EVM, SIWS for Solana)
- Credit 모드: USDC 선충전 → 요청마다 크레딧 차감
- PPU 모드: 요청마다 온체인 USDC 결제

**Payment Modes:**

| Mode | Flow | Best For |
|------|------|----------|
| Credit | SIWX 인증 → USDC 충전 → 크레딧 차감 | 반복적인 API 호출 |
| PPU (Pay-Per-Use) | 요청 → 402 응답 → 건별 USDC 결제 | 일회성 호출 |

**Payment Networks:**

| Network | Use |
|---------|-----|
| Base Mainnet | Production |
| Base Sepolia | Testnet |
| Solana Mainnet | Production |
| Solana Devnet | Testnet |

## Requirements

- **web3-api**: [Nodit](https://nodit.io) API 키 필요 (가입 후 발급)
- **web3-x402**: API 키 불필요, USDC가 있는 지갑 필요

## Links

- [Nodit Developer Docs](https://developer.nodit.io)
- [x402 Protocol](https://www.x402.org/)
- [skills.sh](https://skills.sh)
