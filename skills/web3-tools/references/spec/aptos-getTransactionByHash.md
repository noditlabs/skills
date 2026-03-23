# aptos-getTransactionByHash

> Get transaction by hash

- **Category**: Node API - Aptos (REST)
- **Official Docs**: https://developer.nodit.io/reference/aptos-getTransactionByHash

## Supported Chains

Aptos (mainnet, testnet)

## Endpoint

`GET /transactions/by_hash/{txn_hash}`

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

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `type` | string | Yes | The type of the transaction Enum: `pending_transaction`. |
| `hash` | string | Yes | transaction , 0x 64 hexadecimal string . |
| `sender` | string | Yes | transaction address field. 64 hexadecimal string , 0 0x . |
| `sequence_number` | string | Yes | transaction field. 64 . |
| `max_gas_amount` | string | Yes | transaction gas field. 64 . |
| `gas_unit_price` | string | Yes | transaction gas field. 64 . |
| `expiration_timestamp_secs` | string | Yes | transaction field. 64 . |
| `payload` | object | Yes |  |
| `signature` | object | No |  |
| `replay_protection_nonce` | string | No | transaction replay attack nonce field. 64 . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
