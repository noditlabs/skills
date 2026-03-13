# getAccountStats

> Retrieves statistical information about a specific account including transaction counts, transfer events, and asset holdings.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getAccountStats

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, tron, aptos
- **Networks**: mainnet, sepolia, hoodi, amoy, testnet

## Endpoint
`POST /{chain}/{network}/stats/getAccountStats`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| address | string | Yes | Account address (format varies by chain: EVM 0x+40hex, Tron T+33base58, Aptos 0x+64hex) |

## Response

Response varies by chain:

**EVM chains:**

| Field | Type | Description |
|-------|------|-------------|
| transactionCounts.external | number | External transaction count |
| transactionCounts.internal | number | Internal transaction count (select mainnets only) |
| transferCounts.tokens | number | ERC20 token transfer event count |
| transferCounts.nfts | number | NFT transfer event count |
| assets.tokens | number | Number of ERC20 token types held |
| assets.nfts | number | Number of NFTs held |
| assets.nftContracts | number | Number of NFT contract types held |

**Tron:** Similar structure with TRC10/TRC20 tokens.

**Aptos:** transactionCounts (integer), balanceChangeCounts.tokens, assets.tokens.
