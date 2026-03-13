# getTokenAccountsByAssetType

> Retrieve a list of token accounts for a specific asset type on Aptos. Results are provided based on Object addresses, not Owner addresses.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenAccountsByAssetType

## Supported Chains

| Chain | Networks |
|-------|----------|
| aptos | mainnet, testnet |

## Endpoint

`POST /{chain}/{network}/token/getTokenAccountsByAssetType`

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
| assetType | string | Conditional | Asset type identifier. Use Coin struct format (e.g., `0x1::aptos_coin::AptosCoin`) or Fungible Asset object address. Either `assetType` or `linkedAssetType` is required (mutually exclusive). |
| linkedAssetType | string | Conditional | Common identifier for querying Coin and FA as a single asset unit. Must be the migrated FA object address (0x + 64 hex chars). Either `assetType` or `linkedAssetType` is required (mutually exclusive). |
| page | integer | No | Page number (max 100). Cannot be used with `cursor`. |
| rpp | integer | No | Results per page (1-1000). |
| cursor | string | No | Cursor for pagination. Cannot be used with `page`. |
| withCount | boolean | No | Include total count in response. May slow response. Default: `false`. |

## Response

### Success (200)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| page | integer | No | Page number (only if page > 0 was requested). |
| rpp | integer | No | Results per page. |
| cursor | string | No | Cursor value for next page. |
| count | integer | No | Total count (only if `withCount=true`). |
| items | array | Yes | List of token account records. |

### Items Schema

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| ownerAddress | string | Yes | Account address that owns the asset. |
| objectAddress | string | Yes | Object address where asset is stored. Empty string for Coin (stored directly in account). |
| value | string | Yes | Asset quantity as integer string (no decimals; apply `decimals` for real value). |
| isFrozen | boolean | Yes | Whether the asset is frozen (transfer disabled). |
| isPrimary | boolean | Yes | Whether this object is the primary object for the owner address. |
| assetType | string | Yes | Asset identifier (Coin struct ID or FA object address). |
| tokenStandard | string | Yes | `v1` (Coin) or `v2` (Fungible Asset). |
| linkedAssetType | string | Yes | Common identifier linking migrated Coin/FA pairs. |
