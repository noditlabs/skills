# getLedgersWithinRange

> Get Ledgers Within Range

- **Category**: Data API - Blockchain

## Supported Chains

- xrpl

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/blockchain/getLedgersWithinRange`

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
| `fromLedger` | string | Yes | parameter . input : - **ledger index**: 10 number input - **ledger hash**: 64 hexadecimal string (0x ) - **ledger tag**: "earliest" "latest" input (oldest latest ) : - toLedger , latest result . - fromLedger value toLedger value . - fromLedger toLedger value input , . - fromLedger "latest" toLedger "latest" . |
| `toLedger` | string | Yes | parameter . input : - **ledger index**: 10 number input - **ledger hash**: 64 hexadecimal string (0x ) - **ledger tag**: "earliest" "latest" input (oldest latest ) : - fromLedger , genesis result . - toLedger value fromLedger value . - fromLedger toLedger value input , . - toLedger "earliest" fromLedger "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
