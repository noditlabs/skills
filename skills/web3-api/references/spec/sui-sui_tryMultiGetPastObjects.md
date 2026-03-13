# sui-sui_tryMultiGetPastObjects

> Note there is no software-level guarantee/SLA that objects with past versions can be retrieved by this API, even if the object and version exists/existed. The result may vary across nodes depending on their pruning policies. Return the object information for a specified version

- **Category**: Node API - Sui (JSON-RPC) / Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_tryMultiGetPastObjects

## Supported Chains
sui

## Method
`sui_tryMultiGetPastObjects`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `past_objects` | `array` | required | a vector of object and versions to be queried |
| `options` | `ObjectDataOptions` | optional | options for specifying the content to be returned |

## Returns
`array` - Vec<SuiPastObjectResponse>

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_tryMultiGetPastObjects",
  "params": [
    []
  ]
}
```
