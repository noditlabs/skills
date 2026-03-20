# Supported Chains

Chains and networks available through the x402 proxy. Both Credit and PPU modes support the same chains.

## API Support Summary

| Chain           | Networks                | Data API | Node API |
|-----------------|-------------------------|----------|----------|
| Aptos           | mainnet, testnet        | Yes      | -        |
| Arbitrum        | mainnet, sepolia        | Yes      | Yes      |
| Arc             | testnet                 | Yes      | Yes      |
| Avalanche       | mainnet, fuji           | -        | Yes      |
| Base            | mainnet, sepolia        | Yes      | Yes      |
| Bitcoin         | mainnet                 | Yes      | -        |
| Bitcoincash     | mainnet                 | Yes      | -        |
| BNB             | mainnet, testnet        | Yes      | Yes      |
| Chiliz          | mainnet                 | Yes      | -        |
| Dogecoin        | mainnet                 | Yes      | -        |
| Ethereum        | mainnet, sepolia, hoodi | Yes      | Yes      |
| Ethereumclassic | mainnet                 | Yes      | -        |
| Giwa            | sepolia                 | Yes      | Yes      |
| Kaia            | mainnet, kairos         | Yes      | Yes      |
| Luniverse       | mainnet                 | Yes      | Yes      |
| Optimism        | mainnet, sepolia        | Yes      | Yes      |
| Polygon         | mainnet, amoy           | Yes      | Yes      |
| Solana          | mainnet, devnet         | -        | Yes      |
| Sui             | mainnet                 | -        | Yes      |
| Tron            | mainnet                 | Yes      | -        |
| Xrpl            | mainnet                 | Yes      | -        |

## Payment Networks (for charging credits)

| Network        | Chain ID                                | Use                        |
|----------------|-----------------------------------------|----------------------------|
| Base Mainnet   | eip155:8453                             | Production credit charging |
| Base Sepolia   | eip155:84532                            | Testnet credit charging    |
| Solana Mainnet | solana:5eykt4UsFv8P8NJdTREpY1vzqKqZKvdp | Production credit charging |
| Solana Devnet  | solana:EtWTRABZaYq6iMfeYKouRu166VU2xqa1 | Testnet credit charging    |

Payment networks are for USDC settlement only. They are separate from the API target chains above.
