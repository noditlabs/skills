# getAssetTransfersByAccount

> Get Asset Transfers By Account

- **Category**: Data API - Asset
- **Official Docs**: https://developer.nodit.io/reference/getAssetTransfersByAccount

## Supported Chains

- tron

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/asset/getAssetTransfersByAccount`

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
| `accountAddress` | object | Yes |  |
| `assetIds` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | object | No |  |

## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
