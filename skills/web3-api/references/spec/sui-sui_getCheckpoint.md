# sui-sui_getCheckpoint

> Return a checkpoint

- **Category**: Node API - Sui (JSON-RPC) / Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getCheckpoint

## Supported Chains
sui

## Method
`sui_getCheckpoint`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | `CheckpointId` | required | Checkpoint identifier, can use either checkpoint digest, or checkpoint sequence number as input. |

## Returns
`Checkpoint` - Checkpoint

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getCheckpoint",
  "params": [
    "1000"
  ]
}
```
