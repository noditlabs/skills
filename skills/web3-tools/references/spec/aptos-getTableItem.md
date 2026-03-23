# aptos-getTableItem

> Get table item

- **Category**: Node API - Aptos (REST)
- **Official Docs**: https://developer.nodit.io/reference/aptos-getTableItem

## Supported Chains

Aptos (mainnet, testnet)

## Endpoint

`POST /tables/{table_handle}/item`

## Parameters

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `key_type` | string | Yes | key type |
| `value_type` | string | Yes | value type |
| `key` | string | Yes | table item key value. key_type data . Default: `{"account_address":"0x1","module_name":"0x6170746f735f636f696e","struct_name":"0x4170746f73436f696e"}`. |

## Response

### Success (200) - Successful Response

value_type data .

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
