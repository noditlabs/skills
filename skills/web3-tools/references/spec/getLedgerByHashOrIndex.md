# getLedgerByHashOrIndex

> Get Ledger By Hash Or Index

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/getLedgerByHashOrIndex

## Supported Chains

- xrpl

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/blockchain/getLedgerByHashOrIndex`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `xrpl`. Default: `xrpl`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ledger` | string | Yes | parameter , input . - ledger index: 10 number - ledger hash: 64 hexadecimal string (0x ) - ledger tag: "earliest" "latest" (oldest latest ) Default: `latest`. |

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
