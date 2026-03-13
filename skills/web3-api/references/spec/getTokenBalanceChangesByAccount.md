# getTokenBalanceChangesByAccount

> Retrieve token balance change history for a specific account. Supports IOU tokens on XRPL and fungible tokens on Aptos.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenBalanceChangesByAccount

## Supported Chains

| Chain | Networks |
|-------|----------|
| xrpl | mainnet, testnet |
| aptos | mainnet, testnet |

## Endpoint

`POST /{chain}/{network}/token/getTokenBalanceChangesByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain. Enum: `xrpl`, `aptos` |
| network | string | Yes | Target network. Enum: `mainnet`, `testnet` |

## Request Body

`Content-Type: application/json`

### XRPL

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | No | Account address (Base58, starts with `r`, 25-35 chars). |
| currency | string | No | Currency symbol (e.g., `USD`, `EUR` in ISO-4217 format). |
| issuer | string | No | Issuer account address (Base58, starts with `r`). |
| fromLedger | string | No | Start ledger (ledger index, hash, or tag: `earliest`/`latest`). |
| toLedger | string | No | End ledger (ledger index, hash, or tag: `earliest`/`latest`). |
| fromDate | string | No | Start date in ISO 8601 format. Cannot be used with `fromLedger`/`toLedger`. |
| toDate | string | No | End date in ISO 8601 format. Cannot be used with `fromLedger`/`toLedger`. |

### Aptos

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | No | Account address (0x + 64 hex chars). |
| assetTypes | string | No | Asset type (Coin struct or FA object address). |
| linkedAssetTypes | string | No | Common identifier for querying Coin and FA as a single unit. |
| fromBlock | string | No | Start block (number, hash, or tag: `earliest`/`latest`). |
| toBlock | string | No | End block (number, hash, or tag: `earliest`/`latest`). |
| fromDate | string | No | Start date in ISO 8601 format. Cannot be used with `fromBlock`/`toBlock`. |
| toDate | string | No | End date in ISO 8601 format. Cannot be used with `fromBlock`/`toBlock`. |

### Pagination (both chains)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| page | integer | No | Page number (max 100). Cannot be used with `cursor`. |
| rpp | integer | No | Results per page (1-1000). |
| cursor | string | No | Cursor for pagination. Cannot be used with `page`. |
| withCount | boolean | No | Include total count in response. Default: `false`. |

## Response

### Success (200)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| page | integer | No | Page number. |
| rpp | integer | No | Results per page. |
| cursor | string | No | Cursor for next page. |
| count | integer | No | Total count (only if `withCount=true`). |
| items | array | Yes | List of balance change records. |

### Items Schema (XRPL)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| ledgerIndex | integer | Yes | Ledger sequence number. |
| ledgerTimestamp | integer | Yes | Unix timestamp of ledger close time. |
| transactionIndex | integer | Yes | Transaction index within the ledger. |
| transactionHash | string | Yes | 64-char hex transaction hash. |
| transactionType | string | Yes | Transaction type (e.g., `OfferCreate`, `Payment`). |
| affectedNodesIndex | integer | Yes | Index in the AffectedNodes array. |
| account | string | Yes | Account whose balance changed. |
| currency | string | Yes | Currency code (ISO 4217 or custom hex). |
| issuer | string | Yes | Issuer address (empty for XRP). |
| previousBalance | string | Yes | Balance before the change. |
| finalBalance | string | Yes | Balance after the change. |
| balanceChange | string | Yes | Amount of change (positive = increase, negative = decrease). |

### Items Schema (Aptos)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| blockHeight | integer | No | Block height. |
| blockTimestamp | integer | No | Block timestamp in microseconds (Unix). |
| transactionHash | string | No | Transaction hash (0x + 64 hex). |
| transactionVersion | integer | No | Transaction sequence ID. |
| eventIndex | integer | Yes | Event order index within the transaction. |
| eventType | string | Yes | Event type (Move struct path). |
| subEventIndex | integer | Yes | Sub-event index for multiple asset changes in one event. |
| accountAddress | string | Yes | Account whose balance changed. |
| assetType | string | Yes | Asset type identifier. |
| linkedAssetType | string | Yes | Common Coin/FA identifier. |
| changeValue | string | Yes | Balance change amount (positive = increase, negative = decrease). |
| tokenStandard | string | Yes | `v1` (Coin) or `v2` (Fungible Asset). |
| transferType | string | Yes | Transfer type: `deposit`, `withdraw`, `swap_in`, `swap_out`, `gas_fee`, `refund_gas`. |
