# getNativeTokenBalanceChangesByAccount

> Retrieve native token (XRP) balance change history for a specific account on XRPL.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getNativeTokenBalanceChangesByAccount

## Supported Chains
- xrpl
- Networks: mainnet

## Endpoint
`POST /{chain}/{network}/native/getNativeTokenBalanceChangesByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (xrpl) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | Yes | XRPL account address (r-prefixed, 25-35 char Base58) |
| fromLedger | string | No | Start ledger (index, hash, or tag: earliest/latest) |
| toLedger | string | No | End ledger (index, hash, or tag: earliest/latest) |
| fromDate | string | No | Start date (ISO 8601 format) |
| toDate | string | No | End date (ISO 8601 format) |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (1-1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count (default: false) |

## Response

### 200 OK (Paginated)

Items contain:

| Field | Type | Description |
|-------|------|-------------|
| ledgerIndex | integer | Ledger sequence number |
| ledgerTimestamp | integer | Unix timestamp of ledger close time |
| transactionIndex | integer | Transaction order within ledger |
| transactionHash | string | 64-char hex transaction hash |
| transactionType | string | Transaction type (e.g., Payment, OfferCreate) |
| affectedNodesIndex | integer | Index within AffectedNodes array |
| account | string | Account whose balance changed |
| currency | string | Currency code (e.g., XRP, USD) |
| issuer | string | Asset issuer address (empty for XRP) |
| previousBalance | string | Balance before change |
| finalBalance | string | Balance after change |
| balanceChange | string | Amount changed (signed) |
