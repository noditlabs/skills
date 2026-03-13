# sui-sui_getCheckpoints

> Return paginated list of checkpoints

- **Category**: Node API - Sui (JSON-RPC) / Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getCheckpoints

## Supported Chains
sui

## Method
`sui_getCheckpoints`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | `BigInt_for_uint64` | optional | An optional paging cursor. If provided, the query will start from the next item after the specified cursor. Default to start from the first item if not specified. |
| `limit` | `integer` | optional | Maximum item returned per page, default to [QUERY_MAX_RESULT_LIMIT_CHECKPOINTS] if not specified. |
| `descending_order` | `boolean` | required | query result ordering, default to false (ascending order), oldest record first. |

## Returns
`Page_for_Checkpoint_and_BigInt_for_uint64` - CheckpointPage

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getCheckpoints",
  "params": [
    false
  ]
}
```
