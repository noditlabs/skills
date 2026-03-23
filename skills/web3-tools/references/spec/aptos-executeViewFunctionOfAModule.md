# aptos-executeViewFunctionOfAModule

> Execute view function of a module

- **Category**: Node API - Aptos (REST)
- **Official Docs**: https://developer.nodit.io/reference/aptos-executeViewFunctionOfAModule

## Supported Chains

Aptos (mainnet, testnet)

## Endpoint

`POST /view`

## Parameters

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `function` | string | Yes | deployment module view function input . input . - : {address}::{module_name}::{function_name} |
| `type_arguments` | array | Yes | function type arguments input . gerneric type function , array input. |
| `arguments` | array | Yes | function arguments input . function , array input. |

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
