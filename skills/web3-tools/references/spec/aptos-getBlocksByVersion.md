# aptos-getBlocksByVersion

> Get blocks by version

- **Category**: Node API - Aptos (REST)
- **Official Docs**: https://developer.nodit.io/reference/aptos-getBlocksByVersion

## Supported Chains

Aptos (mainnet, testnet)

## Endpoint

`GET /blocks/by_version/{version}`

## Parameters

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |


## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `block_height` | string | Yes | 64 . JSON u64 value JavaScript . |
| `block_hash` | string | Yes | hashvalue field. |
| `block_timestamp` | string | Yes | creation field. (microseconds) UNIX timestamp , creation . timestamp transaction creation . |
| `first_version` | string | Yes | transaction transaction version number field. Aptos transaction version number , transaction execution . first_version last_version transaction version confirmation . |
| `last_version` | string | Yes | transaction transaction version number field. first_version transaction version , transaction . |
| `transactions` | array | No | transaction . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
