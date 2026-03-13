# getTokenTransfersByCurrencyAndIssuer

> Retrieve token transfer history filtered by currency and issuer on XRPL.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenTransfersByCurrencyAndIssuer

## Supported Chains

| Chain | Networks |
|-------|----------|
| xrpl | mainnet |

## Endpoint

`POST /{chain}/{network}/token/getTokenTransfersByCurrencyAndIssuer`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain. Enum: `xrpl` |
| network | string | Yes | Target network. Enum: `mainnet` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| currency | string | Yes | Currency symbol (ISO 4217 format, e.g., `USD`, `EUR`). |
| issuer | string | No | Issuer account address (Base58, starts with `r`, 25-35 chars). |
| fromLedger | string | No | Start ledger (index, hash, or tag: `earliest`/`latest`). |
| toLedger | string | No | End ledger (index, hash, or tag: `earliest`/`latest`). |
| fromDate | string | No | Start date (ISO 8601). Cannot be used with ledger params. |
| toDate | string | No | End date (ISO 8601). Cannot be used with ledger params. |
| page | integer | No | Page number (max 100). |
| rpp | integer | No | Results per page (1-1000). |
| cursor | string | No | Cursor for pagination. |
| withCount | boolean | No | Include total count. Default: `false`. |

## Response

### Success (200)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| page | integer | No | Page number. |
| rpp | integer | No | Results per page. |
| cursor | string | No | Cursor for next page. |
| count | integer | No | Total count (only if `withCount=true`). |
| items | array | Yes | List of transfer records. |

### Items Schema

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| ledgerIndex | integer | No | Ledger sequence number. |
| ledgerTimestamp | integer | No | Unix timestamp of ledger close time. |
| transactionIndex | integer | No | Transaction index within the ledger. |
| transactionHash | string | No | Transaction hash (64 hex chars). |
| transactionType | string | No | Transaction type (e.g., `Payment`, `OfferCreate`). |
| affectedNodesIndex | integer | Yes | AffectedNodes array index. |
| from | string | Yes | Sender account address. |
| to | string | Yes | Receiver account address. |
| currency | string | Yes | Currency code. |
| issuer | string | Yes | Issuer address (empty for XRP). |
| value | string | Yes | Transfer amount as string. |
