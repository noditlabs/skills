# getTokenBalanceChangesWithinRange

> Retrieve token balance change history within a specific time period or block range on Aptos.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenBalanceChangesWithinRange

## Supported Chains

| Chain | Networks |
|-------|----------|
| aptos | mainnet, testnet |

## Endpoint

`POST /{chain}/{network}/token/getTokenBalanceChangesWithinRange`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain. Enum: `aptos` |
| network | string | Yes | Target network. Enum: `mainnet`, `testnet` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| fromBlock | string | No | Start block (number, hash, or tag: `earliest`/`latest`). Cannot be used with date params. |
| toBlock | string | No | End block (number, hash, or tag: `earliest`/`latest`). Cannot be used with date params. |
| fromDate | string | No | Start date (ISO 8601). Cannot be used with block params. |
| toDate | string | No | End date (ISO 8601). Cannot be used with block params. |
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
| items | array | Yes | List of balance change records. |

### Items Schema

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
| changeValue | string | Yes | Balance change amount (positive/negative). |
| tokenStandard | string | Yes | `v1` (Coin) or `v2` (Fungible Asset). |
| transferType | string | Yes | Transfer type: `deposit`, `withdraw`, `swap_in`, `swap_out`, `gas_fee`, `refund_gas`. |
