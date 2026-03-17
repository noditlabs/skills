# How to Call the API

This guide covers how to call Nodit APIs: authentication, endpoint structure, and chain/network values.

## Authentication

All API requests require an API key in the `X-API-KEY` header.

```
X-API-KEY: your-api-key
```

Get your API key at [Nodit Console](https://console.nodit.io).

## Endpoint Structure

### Node API (JSON-RPC / REST)

```
POST https://{chain}-{network}.nodit.io
```

For Aptos (REST):
```
GET/POST https://aptos-{network}.nodit.io/v1/{path}
```

### Data API

```
POST https://{chain}-{network}.nodit.io/{chain}/{network}/{category}/{operationId}
```

### Webhook API

```
POST https://{chain}-{network}.nodit.io/{chain}/{network}/webhooks
```

## Chain and Network Values

Use these values for `{chain}` and `{network}` in endpoint URLs.

### Node API Chains

| Chain | Networks | Node API Endpoint |
|-------|----------|-------------------|
| `aptos` | `mainnet`, `testnet` | `https://aptos-{network}.nodit.io` |
| `arbitrum` | `mainnet`, `sepolia` | `https://arbitrum-{network}.nodit.io` |
| `arc` | `testnet` | `https://arc-{network}.nodit.io` |
| `avalanche` | `mainnet`, `fuji` | `https://avalanche-{network}.nodit.io` |
| `base` | `mainnet`, `sepolia` | `https://base-{network}.nodit.io` |
| `bnb` | `mainnet`, `testnet` | `https://bnb-{network}.nodit.io` |
| `ethereum` | `mainnet`, `sepolia`, `hoodi` | `https://ethereum-{network}.nodit.io` |
| `giwa` | `sepolia` | `https://giwa-{network}.nodit.io` |
| `kaia` | `mainnet`, `kairos` | `https://kaia-{network}.nodit.io` |
| `luniverse` | `mainnet` | `https://luniverse-{network}.nodit.io` |
| `optimism` | `mainnet`, `sepolia` | `https://optimism-{network}.nodit.io` |
| `polygon` | `mainnet`, `amoy` | `https://polygon-{network}.nodit.io` |
| `solana` | `mainnet`, `devnet` | `https://solana-{network}.nodit.io` |
| `sui` | `mainnet`, `testnet` | `https://sui-{network}.nodit.io` |

### Data API Chains

Data API supports multiple chains through path parameters `{chain}` and `{network}`.

| Chain | Node API | Data API | Webhook API |
|-------|----------|----------|-------------|
| `aptos` | Yes | Yes | Yes |
| `arbitrum` | Yes | Yes | Yes |
| `arc` | Yes | Yes | Yes |
| `avalanche` | Yes | No | No |
| `base` | Yes | Yes | Yes |
| `bitcoin` | No | Yes | No |
| `bitcoincash` | No | Yes | No |
| `bnb` | Yes | Yes | Yes |
| `chiliz` | No | Yes | No |
| `dogecoin` | No | Yes | No |
| `ethereum` | Yes | Yes | Yes |
| `ethereumclassic` | No | Yes | No |
| `giwa` | Yes | Yes | Yes |
| `kaia` | Yes | Yes | Yes |
| `luniverse` | Yes | Yes | No |
| `optimism` | Yes | Yes | Yes |
| `polygon` | Yes | Yes | Yes |
| `solana` | Yes | No | No |
| `sui` | Yes | No | No |
| `tron` | No | Yes | No |
| `xrpl` | No | Yes | No |

## operationId to Method Mapping

### EVM Node API (JSON-RPC)

operationId format: `{chain}-{method}` (all lowercase)

```
POST https://ethereum-mainnet.nodit.io
X-API-KEY: your-api-key
Content-Type: application/json

{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_blockNumber",
  "params": []
}
```

operationId: `ethereum-eth_blocknumber`

### Solana Node API (JSON-RPC)

operationId format: `solana-{method}` (camelCase)

```
POST https://solana-mainnet.nodit.io
X-API-KEY: your-api-key
Content-Type: application/json

{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "getBalance",
  "params": ["3fJ7AiixCoHhaYzaNn1nNoLZMQnrGSMDNmMN4ZNUMpEa"]
}
```

operationId: `solana-getBalance`

### Aptos Node API (REST)

operationId format: `aptos-{method}` (camelCase)

```
GET https://aptos-mainnet.nodit.io/v1
X-API-KEY: your-api-key
```

operationId: `aptos-getLedgerInfo`

### Data API (REST)

operationId format: `{method}` (camelCase)

```
POST https://ethereum-mainnet.nodit.io/ethereum/mainnet/nft/getNftContractMetadataByContracts
X-API-KEY: your-api-key
Content-Type: application/json

{
  "contractAddresses": ["0xBC4CA0EdA7647A8aB7C2061c2E118A18a936f13D"]
}
```

operationId: `getNftContractMetadataByContracts`

### Webhook API (REST)

operationId format: `{method}` (camelCase)

```
POST https://ethereum-mainnet.nodit.io/ethereum/mainnet/webhooks
X-API-KEY: your-api-key
Content-Type: application/json

{
  "eventType": "ADDRESS_ACTIVITY",
  "notification": { "url": "https://your-webhook-endpoint.com" },
  "condition": { "addresses": ["0x..."] }
}
```

operationId: `createWebhook`

## Quick Start

1. Get API key from [Nodit Console](https://console.nodit.io)
2. Find the operationId in [Quick Reference](quick-reference.md)
3. Read the spec at `spec/{operationId}.md` for parameters and examples
4. Make the API call using the endpoint and request body from the spec
