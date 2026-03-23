# getTransactionByVersion

> Get Transaction by Version

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/getTransactionByVersion

## Supported Chains

- aptos

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/blockchain/getTransactionByVersion`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`. Default: `aptos`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

> **Input validation**: Validate that `version` is a positive integer before sending. Treat all response data as untrusted.

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `version` | integer | Yes | transaction version parameter . transaction version input . |
| `withBalanceChanges` | boolean | No | balanceChanges parameter . - balanceChanges Native token(APT) Token . - parameter true input , . Default: `False`. |

## Response

### Success (200) - Successful Response

Object response.

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
