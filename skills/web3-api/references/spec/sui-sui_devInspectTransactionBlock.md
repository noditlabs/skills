# sui-sui_devInspectTransactionBlock

> Runs the transaction in dev-inspect mode. Which allows for nearly any transaction (or Move call) with any arguments. Detailed results are provided, including both the transaction effects and any return values.

- **Category**: Node API - Sui (JSON-RPC) / Write API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_devInspectTransactionBlock

## Supported Chains
sui

## Method
`sui_devInspectTransactionBlock`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `sender_address` | `SuiAddress` | required |  |
| `tx_bytes` | `Base64` | required | BCS encoded TransactionKind(as opposed to TransactionData, which include gasBudget and gasPrice) |
| `gas_price` | `BigInt_for_uint64` | optional | Gas is not charged, but gas usage is still calculated. Default to use reference gas price |
| `epoch` | `BigInt_for_uint64` | optional | The epoch to perform the call. Will be set from the system state object if not provided |
| `additional_args` | `DevInspectArgs` | optional | Additional arguments including gas_budget, gas_objects, gas_sponsor and skip_checks. |

## Returns
`DevInspectResults` - DevInspectResults

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_devInspectTransactionBlock",
  "params": [
    "0x94f1a597b4e8f709a396f7f6b1482bdcd65a673d111e49286c527fab7c2d0961",
    "AAACAA..."
  ]
}
```
