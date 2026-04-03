# aptos-estimateGasPrice

> Estimate gas price

- **Category**: Node API - Aptos (REST)

## Supported Chains

Aptos (mainnet, testnet)

## Endpoint

`GET /estimate_gas_price`

## Parameters

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |


## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `deprioritized_gas_estimate` | integer | No | value |
| `gas_estimate` | integer | Yes | value |
| `prioritized_gas_estimate` | integer | No | value |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
