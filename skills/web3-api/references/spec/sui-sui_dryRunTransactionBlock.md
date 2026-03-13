# sui-sui_dryRunTransactionBlock

> Return transaction execution effects including the gas cost summary, while the effects are not committed to the chain.

- **Category**: Node API - Sui (JSON-RPC) / Write API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_dryRunTransactionBlock

## Supported Chains
sui

## Method
`sui_dryRunTransactionBlock`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `tx_bytes` | `Base64` | required |  |

## Returns
`DryRunTransactionBlockResponse` - DryRunTransactionBlockResponse

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_dryRunTransactionBlock",
  "params": [
    "AAACAA..."
  ]
}
```
