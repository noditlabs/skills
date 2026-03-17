# Supported Chains

Chains and networks available through the x402 proxy. Both Credit and PPU modes support the same chains.

## API Support Summary

| Chain | Networks | Data API | Node API |
|-------|----------|----------|----------|
| Arbitrum | mainnet, sepolia | Yes | Yes |
| Arc | testnet | - | Yes |
| Avalanche | mainnet, fuji | - | Yes |
| Base | mainnet, sepolia | Yes | Yes |
| BNB | mainnet, testnet | Yes | Yes |
| Ethereum | mainnet, sepolia, hoodi | Yes | Yes |
| Giwa | sepolia | - | Yes |
| Kaia | mainnet, kairos | Yes | Yes |
| Luniverse | mainnet | - | Yes |
| Optimism | mainnet, sepolia | Yes | Yes |
| Polygon | mainnet, amoy | Yes | Yes |
| Solana | mainnet, devnet | Yes | Yes |
| Sui | mainnet | Yes | Yes |

**Total:** 13 chains, 24 network combinations.

## Payment Networks (for charging credits)

| Network | Chain ID | Use |
|---------|----------|-----|
| Base Mainnet | eip155:8453 | Production credit charging |
| Base Sepolia | eip155:84532 | Testnet credit charging |
| Solana Mainnet | solana:5eykt4UsFv8P8NJdTREpY1vzqKqZKvdp | Production credit charging |
| Solana Devnet | solana:EtWTRABZaYq6iMfeYKouRu166VU2xqa1 | Testnet credit charging |

Payment networks are for USDC settlement only. They are separate from the API target chains above.
