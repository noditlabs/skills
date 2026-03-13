# getTokenMetadataByAssetTypes

> Retrieve metadata for tokens with specific asset types on Aptos.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenMetadataByAssetTypes

## Supported Chains

| Chain | Networks |
|-------|----------|
| aptos | mainnet, testnet |

## Endpoint

`POST /{chain}/{network}/token/getTokenMetadataByAssetTypes`

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
| assetTypes | string[] | No | Array of asset types to query (1-1000 items). Coin struct format or FA object address. |
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
| items | array | Yes | List of token metadata records. |

### Items Schema

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| assetType | string | No | Asset identifier (Coin struct or FA object address). |
| tokenStandard | string | No | `v1` (Coin) or `v2` (Fungible Asset). |
| name | string | Yes | Token name. |
| symbol | string | Yes | Token symbol. |
| decimals | integer | Yes | Decimal places for display. |
| totalSupply | string | Yes | Current circulating supply (raw integer, apply decimals). |
| maximumSupply | string | Yes | Maximum supply (empty string = unlimited). |
| creatorAddress | string | Yes | Address of the asset creator. |
| projectURI | string | Yes | Project information URI. |
| iconURI | string | Yes | Token icon image URL. |
