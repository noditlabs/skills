# searchAssetMetadataByKeyword

> Searches TRC10 token metadata by name or symbol keyword.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/searchAssetMetadataByKeyword

## Supported Chains
- tron
- **Networks**: mainnet

## Endpoint
`POST /{chain}/{network}/asset/searchAssetMetadataByKeyword`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (tron) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| keyword | string | Yes | Token name or symbol to search for |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (max 1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count. Default: false |

## Response

| Field | Type | Description |
|-------|------|-------------|
| page | integer | Current page number |
| rpp | integer | Results per page |
| cursor | string | Next page cursor |
| count | integer | Total count (if withCount=true) |
| items | array | List of TRC10 metadata objects (id, name, symbol, totalSupply, decimals, startTime, endTime, description, url, blockNumber, blockTimestamp, transactionHash, deployer, trxNum, num) |
