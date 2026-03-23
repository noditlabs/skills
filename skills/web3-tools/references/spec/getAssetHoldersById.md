# getAssetHoldersById

> Get Asset Holders By ID

- **Category**: Data API - Asset
- **Official Docs**: https://developer.nodit.io/reference/getAssetHoldersById

## Supported Chains

- tron

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/asset/getAssetHoldersById`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `tron`. Default: `tron`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `assetId` | integer | Yes | Asset ID input . Asset ID 0 . |
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
| `ownerAddress` | string | Yes | (TRON) address . address "T" 34 Base58 . |
| `balance` | string | Yes | balance. value 10 , TRX SUN(1 TRX = 1,000,000 SUN). |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
