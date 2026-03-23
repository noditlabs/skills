# aptos-waitForTransactionByHash

> Wait for transaction by hash

- **Category**: Node API - Aptos (REST)
- **Official Docs**: https://developer.nodit.io/reference/aptos-waitForTransactionByHash

## Supported Chains

Aptos (mainnet, testnet)

## Endpoint

`GET /transactions/wait_by_hash/{txn_hash}`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `txn_hash` | string | Yes | transaction hashvalue |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |


## Response

### Success (200) - Successful Response

Array response.

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
