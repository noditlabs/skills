# getTransactionsInLedger

> Retrieves all transactions contained in a specific XRPL ledger.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getTransactionsInLedger

## Supported Chains
- xrpl
- **Networks**: mainnet

## Endpoint
`POST /{chain}/{network}/blockchain/getTransactionsInLedger`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (xrpl) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| ledger | string | No | Ledger to query (ledger index, ledger hash, or tag like "validated"/"closed"/"current") |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (max 1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count. Default: false |
| withBalanceChanges | boolean | No | Include balance changes (XRP and IOU tokens). May slow response |
| withTokenTransfers | boolean | No | Include IOU token transfer details. May slow response |

## Response

| Field | Type | Description |
|-------|------|-------------|
| page | integer | Current page number |
| rpp | integer | Results per page |
| cursor | string | Next page cursor |
| count | integer | Total count (if withCount=true) |
| items | array | List of XRPL transaction objects |
