# getAssetTransfersByAccount

> Retrieves TRC10 token transfer history for a specific account (sent or received).

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getAssetTransfersByAccount

## Supported Chains
- tron
- **Networks**: mainnet

## Endpoint
`POST /{chain}/{network}/asset/getAssetTransfersByAccount`

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
| assetIds | array | No | Filter by specific Asset IDs |
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

| Field | Type | Description |
|-------|------|-------------|
| page | integer | Current page number |
| rpp | integer | Results per page |
| cursor | string | Next page cursor |
| count | integer | Total count (if withCount=true) |
| items | array | List of transfer objects |
| items[].from | string | Sender address |
| items[].to | string | Receiver address |
| items[].value | string | Transfer amount |
| items[].blockTimestamp | integer | Block timestamp (UNIX ms) |
| items[].blockNumber | integer | Block number |
| items[].transactionHash | string | Transaction hash |
| items[].transactionIndex | integer | Transaction index in block |
| items[].internalTransactionIndex | integer | Internal tx index (-1 = root) |
| items[].exchangeId | integer | DEX exchange ID (null if not a swap) |
| items[].asset | object | TRC10 metadata (id, name, symbol, etc.) |
