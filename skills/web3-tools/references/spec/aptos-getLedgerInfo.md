# aptos-getLedgerInfo

> Get ledger info

- **Category**: Node API - Aptos (REST)
- **Official Docs**: https://developer.nodit.io/reference/aptos-getLedgerInfo

## Supported Chains

Aptos (mainnet, testnet)

## Endpoint

`GET /`

## Parameters

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |


## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `chain_id` | integer | Yes | The identifier number of the current chain. |
| `epoch` | string | Yes | The current consensus epoch number based on the validator set for that period. |
| `ledger_version` | string | Yes | The ledger version of the latest transaction. |
| `oldest_ledger_version` | string | Yes | The ledger version of the oldest transaction. |
| `ledger_timestamp` | string | Yes | The ledger timestamp indicating when the current ledger was created. |
| `node_role` | string | Yes | The node role (full_node, validator). |
| `oldest_block_height` | string | Yes | The oldest block height. |
| `block_height` | string | Yes | The latest block height. |
| `git_hash` | string | No | The Git hash of the built API endpoint. Used to verify the exact software version used by the API endpoint. |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
