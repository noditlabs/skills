# aptos-getAccountResource

> Get account resource

- **Category**: Node API - Aptos (REST)
- **Official Docs**: https://developer.nodit.io/reference/aptos-getAccountResource

## Supported Chains

Aptos (mainnet, testnet)

## Endpoint

`GET /accounts/{address}/resources/{resource_type}`

## Parameters

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |


## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `type` | string | No | Move . MoveStructTag (path) (query) parameter . ( : get_events_by_event_handle ) value : 1. move_module_address, module_name, struct_name (::) 2. parameter (,) : - `0x1::coin::CoinStore<0x1::aptos_coin::aptosCoin>` - `0x1::account::Account` |
| `data` | object | No | JSON data . key JSON value/object . - Move bool : boolean . - u8~i32: integer . - u64~i256: string . - address: HexEncodedBytes string( : 0x1) . - : object(object) . - vector: array(array) . - , vector<u8> 0x HexEncodedBytes string . - 0x1::string::String: string . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
