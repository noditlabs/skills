# Nodit Skills

[Nodit](https://nodit.io) blockchain API skills for AI coding agents. Query on-chain data across 30+ chains directly from your IDE.

## Installation

via [skills.sh](https://skills.sh):

```bash
npx skills add noditlabs/skills --yes
```

Or install a specific skill:

```bash
npx skills add noditlabs/skills --skill web3-tools
npx skills add noditlabs/skills --skill web3-x402
```

## Skills

### `web3-tools`

Multi-chain blockchain data querying skill powered by the Nodit API. Requires an API key for authentication.

**Use when:**
- Querying token / NFT balances and metadata
- Looking up transactions and analyzing transfer history
- Fetching block data
- Reading smart contract state (eth_call)
- Resolving ENS names
- Monitoring on-chain events (Webhook)
- Estimating and checking gas fees
- Analyzing token holders and transfer history

**Supported APIs:**

| API Type | Description | Format |
|----------|-------------|--------|
| Data API | Indexed blockchain data (balances, NFTs, tokens, statistics, etc.) | REST |
| Node API | Direct blockchain node calls (JSON-RPC) | JSON-RPC |
| Aptos Indexer API | Indexed Aptos data | GraphQL |
| Webhook API | On-chain event subscription management | REST |

**Supported Chains:**

Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc, Chiliz, Ethereum Classic, Solana, Sui, Aptos, Bitcoin, Bitcoin Cash, Dogecoin, Tron, XRPL

---

### `web3-x402`

Access the Nodit API without an API key — pay with USDC via the [x402 protocol](https://www.x402.org/) instead.

Works alongside the `web3-tools` skill: this skill handles wallet-based authentication and billing, while `web3-tools` provides the API specs and parameters.

**Use when:**
- Querying blockchain data without an API key
- Building autonomous agents that call APIs with wallet-based auth
- Using SIWX authentication (SIWE for EVM, SIWS for Solana)
- Credit mode: pre-charge USDC, then deduct credits per request
- PPU mode: pay on-chain USDC per individual request

**Payment Modes:**

| Mode | Flow | Best For |
|------|------|----------|
| Credit | SIWX auth → charge USDC → deduct credits per call | Repeated API usage |
| PPU (Pay-Per-Use) | Request → 402 response → pay per request | One-off calls |

**Payment Networks:**

| Network | Use |
|---------|-----|
| Base Mainnet | Production |
| Base Sepolia | Testnet |
| Solana Mainnet | Production |
| Solana Devnet | Testnet |

## Requirements

- **web3-tools**: Requires a [Nodit](https://nodit.io) API key (free sign-up)
- **web3-x402**: No API key needed — requires a wallet with USDC

## Links

- [Nodit Developer Docs](https://developer.nodit.io)
- [x402 Protocol](https://www.x402.org/)
- [Agent Skills Specification](https://agentskills.io)
- [skills.sh](https://skills.sh)

## License

MIT
