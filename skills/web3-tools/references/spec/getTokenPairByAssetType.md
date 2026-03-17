# getTokenPairByAssetType

> Get Token Pair by Asset Type

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenPairByAssetType

## Supported Chains

- aptos

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/token/getTokenPairByAssetType`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`. Default: `aptos`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `assetType` | string | Yes | parameter . 64 hexadecimal("0x" ) input , : - Coin: "0x1::aptos_coin::AptosCoin" Struct ID - Fungible Asset: Token Metadata Object address |

## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `coinAssetType` | string | Yes | Coin field. Coin 'moduleaddress::module :: ' . |
| `fungibleAssetType` | string | Yes | Fungible Asset field. Fungible Asset 0x 64 hexadecimal string , data Object address . |
| `linkedAssetType` | string | Yes | Coin Fungible Asset , . Coin/Fungible Asset key , Fungible Asset Metadata Object address . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
