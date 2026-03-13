# sui-sui_multiGetTransactionBlocks

> Returns an ordered list of transaction responses The method will throw an error if the input contains any duplicate or the input size exceeds QUERY_MAX_RESULT_LIMIT

- **Category**: Node API - Sui (JSON-RPC) / Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_multiGetTransactionBlocks

## Supported Chains
sui

## Method
`sui_multiGetTransactionBlocks`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `digests` | `array` | required | A list of transaction digests. |
| `options` | `TransactionBlockResponseOptions` | optional | config options to control which fields to fetch |

## Returns
`array` - Vec<SuiTransactionBlockResponse>

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_multiGetTransactionBlocks",
  "params": [
    []
  ]
}
```
