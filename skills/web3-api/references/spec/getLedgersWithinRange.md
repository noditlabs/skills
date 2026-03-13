# getLedgersWithinRange

> Retrieve a list of XRP Ledgers within a specified time period or ledger range.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getLedgersWithinRange

## Supported Chains
- xrpl
- Networks: mainnet

## Endpoint
`POST /{chain}/{network}/blockchain/getLedgersWithinRange`

## Parameters

### Path Parameters

| Name | Type | Required | Description |ㄴ
|------|------|----------|-------------|
| chain | string | Yes | Target chain (xrpl) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| fromLedger | string | No | Start ledger (index, hash, or tag: earliest/latest) |
| toLedger | string | No | End ledger (index, hash, or tag: earliest/latest) |
| fromDate | string | No | Start date (ISO 8601). Cannot be used with fromLedger/toLedger. |
| toDate | string | No | End date (ISO 8601). Cannot be used with fromLedger/toLedger. |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (1-1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count (default: false) |

## Response

### 200 OK (Paginated)

Items follow the same schema as `getLedgerByHashOrIndex`:

| Field | Type | Description |
|-------|------|-------------|
| ledgerHash | string | Ledger hash (64-char hex) |
| ledgerIndex | integer | Ledger sequence number |
| ledgerTimestamp | integer | Unix timestamp |
| parentLedgerHash | string | Previous ledger hash |
| accountHash | string | Account states hash |
| totalCoins | string | Total XRP |
| transactionHash | string | Merkle root of transactions |
| transactionCount | integer | Number of transactions |
| transactions | array | Transaction hashes |
