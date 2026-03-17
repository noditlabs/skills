# getTokenAccountsByAssetType

> Get Token Accounts by Asset Type

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenAccountsByAssetType

## Supported Chains

- aptos

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/token/getTokenAccountsByAssetType`

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
| `assetType` | object | No |  |
| `linkedAssetType` | string | No | Coin FA(Fungible Asset) . linkedAssetType FA Object address input , 64 hexadecimal("0x" ) input . |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |

## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. 0x 64 hexadecimal string , . Coin account address, Fungible Asset Object address . |
| `objectAddress` | string | Yes | Object address field. : - Coin: ("") - Fungible Asset: token Object address (0x 64 hexadecimal string) |
| `value` | string | Yes | field. , . value decimals . |
| `isFrozen` | boolean | Yes | field. true . status confirmation . |
| `isPrimary` | boolean | Yes | Object Owner address Object field. true Object Owner address Object . |
| `assetType` | string | Yes | field. : - Coin: Move ID ( : 0x1::aptos_coin::AptosCoin) - Fungible Asset: data Object address |
| `tokenStandard` | string | Yes | field. - v1: Coin - v2: Fungible Asset |
| `linkedAssetType` | string | Yes | Coin Fungible Asset , . Coin/Fungible Asset key , Fungible Asset Metadata Object address . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
