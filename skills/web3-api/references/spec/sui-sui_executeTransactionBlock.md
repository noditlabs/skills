# sui-sui_executeTransactionBlock

> Execute the transaction and wait for results if desired. Request types: 1. WaitForEffectsCert: waits for TransactionEffectsCert and then return to client.     This mode is a proxy for transaction finality. 2. WaitForLocalExecution: waits for TransactionEffectsCert and make sure the node     executed the transaction locally before returning the client. The local execution     makes sure this node is aware of this transaction when client fires subsequent queries.     However if the node fails to execute the transaction locally in a timely manner,     a bool type in the response is set to false to indicated the case. request_type is default to be `WaitForEffectsCert` unless options.show_events or options.show_effects is true

- **Category**: Node API - Sui (JSON-RPC) / Write API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_executeTransactionBlock

## Supported Chains
sui

## Method
`sui_executeTransactionBlock`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `tx_bytes` | `Base64` | required | BCS serialized transaction data bytes without its type tag, as base-64 encoded string. |
| `signatures` | `array` | required | A list of signatures (`flag || signature || pubkey` bytes, as base-64 encoded string). Signature is committed to the intent message of the transaction data, as base-64 encoded string. |
| `options` | `TransactionBlockResponseOptions` | optional | options for specifying the content to be returned |
| `request_type` | `ExecuteTransactionRequestType` | optional | The request type, derived from `SuiTransactionBlockResponseOptions` if None |

## Returns
`TransactionBlockResponse` - SuiTransactionBlockResponse

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_executeTransactionBlock",
  "params": [
    "AAACAA...",
    []
  ]
}
```
