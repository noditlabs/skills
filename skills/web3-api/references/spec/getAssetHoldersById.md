# getAssetHoldersById

> Retrieves a list of accounts holding a specific TRC10 token by its Asset ID.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getAssetHoldersById

## Supported Chains
- tron
- **Networks**: mainnet

## Endpoint
`POST /{chain}/{network}/asset/getAssetHoldersById`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (tron) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| assetId | integer | Yes | TRC10 Asset ID (positive integer) |
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
| items | array | List of holder objects |
| items[].ownerAddress | string | Tron address (T + 33 Base58) |
| items[].balance | string | Current balance in SUN (1 TRX = 1,000,000 SUN) |
