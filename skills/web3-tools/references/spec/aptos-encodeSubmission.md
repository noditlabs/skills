# aptos-encodeSubmission

> Encode submission

- **Category**: Node API - Aptos (REST)
- **Official Docs**: https://developer.nodit.io/reference/aptos-encodeSubmission

## Supported Chains

Aptos (mainnet, testnet)

## Endpoint

`POST /transactions/encode_submission`

## Parameters

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `sender` | string | Yes | transaction address field. 64 hexadecimal string , 0 0x . |
| `sequence_number` | string | Yes | transaction field. 64 . |
| `max_gas_amount` | string | Yes | transaction gas field. 64 . |
| `gas_unit_price` | string | Yes | transaction gas field. 64 . |
| `expiration_timestamp_secs` | string | Yes | transaction field. 64 . |
| `payload` | object | Yes | transaction payload field. |
| `replay_protection_nonce` | string | Yes | transaction replay attack nonce field. 64 . |
| `signature` | object | Yes | transaction signature field. Ed25519, MultiEd25519, MultiAgent, FeePayer, Account, NoAccount . |

## Response

### Success (200) - Successful Response

0x hexadecimal string encoding BCS transaction is returned. value signature Submit Transaction API transaction .

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
