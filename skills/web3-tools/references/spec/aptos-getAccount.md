# aptos-getAccount

> Get account

- **Category**: Node API - Aptos (REST)

## Supported Chains

Aptos (mainnet, testnet)

## Endpoint

`GET /accounts/{address}`

## Parameters

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |


## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `sequence_number` | string | No | transaction field. 64 . |
| `authentication_key` | string | No | byte(Vec) data 0x hexadecimal encoding , byte hexadecimal . Address , HexEncodedBytes 0 . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
