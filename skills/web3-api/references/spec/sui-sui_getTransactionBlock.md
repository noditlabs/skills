# sui-sui_getTransactionBlock

> Return the transaction response object.

- **Category**: Node API - Sui (JSON-RPC) / Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getTransactionBlock

## Supported Chains
sui

## Method
`sui_getTransactionBlock`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `digest` | `TransactionDigest` | required | the digest of the queried transaction |
| `options` | `TransactionBlockResponseOptions` | optional | options for specifying the content to be returned |

## Returns
`TransactionBlockResponse` - SuiTransactionBlockResponse

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getTransactionBlock",
  "params": [
    "4vJ9JU1bJJE96FWSJKvHsmmFADCg4GPZQfc1hab3Gkhm"
  ]
}
```
