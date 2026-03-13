# sui-sui_multiGetObjects

> Return the object data for a list of objects

- **Category**: Node API - Sui (JSON-RPC) / Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_multiGetObjects

## Supported Chains
sui

## Method
`sui_multiGetObjects`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `object_ids` | `array` | required | the IDs of the queried objects |
| `options` | `ObjectDataOptions` | optional | options for specifying the content to be returned |

## Returns
`array` - Vec<SuiObjectResponse>

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_multiGetObjects",
  "params": [
    []
  ]
}
```
