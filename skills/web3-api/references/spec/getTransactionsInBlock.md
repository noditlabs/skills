# getTransactionsInBlock

> Retrieves all transactions contained in a specific block.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getTransactionsInBlock

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, tron, aptos
- **Networks**: mainnet, testnet, sepolia, hoodi, amoy, shasta

## Endpoint
`POST /{chain}/{network}/blockchain/getTransactionsInBlock`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network |

## Request Body

Schema varies by chain. Common fields:

| Name | Type | Required | Description |
|------|------|----------|-------------|
| blockNumber / blockHeight | integer/string | Yes (one of) | Block number or height to query |
| blockHash | string | No | Block hash (alternative to number) |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (max 1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count. Default: false |
| withLogs | boolean | No | Include event logs (EVM chains) |
| withDecode | boolean | No | Include decoded data (EVM chains) |

## Response

| Field | Type | Description |
|-------|------|-------------|
| page | integer | Current page number |
| rpp | integer | Results per page |
| cursor | string | Next page cursor |
| count | integer | Total count (if withCount=true) |
| items | array | List of transaction objects (schema varies by chain) |
