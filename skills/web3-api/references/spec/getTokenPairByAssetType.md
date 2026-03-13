# getTokenPairByAssetType

> Look up a token pair by asset type on Aptos. Token pairs consist of a Coin and a Fungible Asset that share the same linkedAssetType after migration.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenPairByAssetType

## Supported Chains

| Chain | Networks |
|-------|----------|
| aptos | mainnet, testnet |

## Endpoint

`POST /{chain}/{network}/token/getTokenPairByAssetType`

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
| assetType | string | Yes | Asset type to look up. Coin struct format (e.g., `0x1::aptos_coin::AptosCoin`) or FA object address. |

## Response

### Success (200)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| coinAssetType | string | Yes | Coin standard asset type (`address::module::struct` format). |
| fungibleAssetType | string | Yes | Fungible Asset standard type (0x + 64 hex, metadata object address). |
| linkedAssetType | string | Yes | Common identifier linking the Coin/FA pair (migrated FA metadata object address). |
