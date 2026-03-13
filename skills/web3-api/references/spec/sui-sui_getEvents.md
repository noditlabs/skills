# sui-sui_getEvents

> Return transaction events.

- **Category**: Node API - Sui (JSON-RPC) / Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getEvents

## Supported Chains
sui

## Method
`sui_getEvents`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `transaction_digest` | `TransactionDigest` | required | the event query criteria. |

## Returns
`array` - Vec<SuiEvent>

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getEvents",
  "params": [
    "4vJ9JU1bJJE96FWSJKvHsmmFADCg4GPZQfc1hab3Gkhm"
  ]
}
```
