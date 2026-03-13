# getAssetsOwnedByAccount

> Retrieves TRC10 tokens owned by a specific account.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getAssetsOwnedByAccount

## Supported Chains
- tron
- **Networks**: mainnet

## Endpoint
`POST /{chain}/{network}/asset/getAssetsOwnedByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (tron) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| accountAddress | string | Yes | Tron account address (T + 33 Base58) |
| assetIds | array | No | Filter by specific Asset IDs (positive integers) |
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
| items | array | List of owned asset objects |
| items[].ownerAddress | string | Account address |
| items[].balance | string | Current balance |
| items[].asset | object | TRC10 metadata (id, name, symbol, totalSupply, decimals, etc.) |
