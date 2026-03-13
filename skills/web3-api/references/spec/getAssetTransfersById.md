# getAssetTransfersById

> Retrieves transfer history for a specific TRC10 token by its Asset ID.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getAssetTransfersById

## Supported Chains
- tron
- **Networks**: mainnet

## Endpoint
`POST /{chain}/{network}/asset/getAssetTransfersById`

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
| fromBlock | string | No | Start block (number, hash, or "earliest") |
| toBlock | string | No | End block (number, hash, or "latest") |
| fromDate | string | No | Start date (ISO 8601). Cannot be used with block params |
| toDate | string | No | End date (ISO 8601). Cannot be used with block params |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (max 1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count. Default: false |
| withZeroValue | boolean | No | Include zero-value transfers. Default: false |

## Response

Paginated list with items containing: from, to, value, blockTimestamp, blockNumber, transactionHash, transactionIndex, internalTransactionIndex, exchangeId, and asset metadata object.
