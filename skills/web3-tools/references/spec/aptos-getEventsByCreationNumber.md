# aptos-getEventsByCreationNumber

> Get events by creation number

- **Category**: Node API - Aptos (REST)
- **Official Docs**: https://developer.nodit.io/reference/aptos-getEventsByCreationNumber

## Supported Chains

Aptos (mainnet, testnet)

## Endpoint

`GET /accounts/{address}/events/{creation_number}`

## Parameters

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |


## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `version` | string | No | transaction version ID , 0 . transaction version transaction execution transaction status . |
| `guid` | object | Yes |  |
| `sequenceNumber` | string | Yes | transaction field. 64 . |
| `type` | string | Yes | transaction payload Move . value: - `bool` - `u8` - `u16`,`u32`,`u64`,`u128`,`u256` - `i8`,`i16`,`i32`,`i64`,`i128`,`i256` - `address` - `signer` - `vector: vector<{non-reference MoveTypeId}>` - `struct: {address}::{module_name}::{struct_name}::<{generic types}>` Vector value : - `vector<u8>` - `vector<vector<u64>>` - `vector<0x1::coin::CoinStore<0x1::aptos_coin::AptosCoin>>` Struct value : - `0x1::coin::CoinStore<0x1::aptos_coin::AptosCoin>` - `0x1::account::Account` : 1. 2 struct tag id . 2. URL url-encoding(AKA percent-encoding) encoding . |
| `data` | object | Yes |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
