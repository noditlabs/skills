# sui-sui_tryGetPastObject

> Note there is no software-level guarantee/SLA that objects with past versions can be retrieved by this API, even if the object and version exists/existed. The result may vary across nodes depending on their pruning policies. Return the object information for a specified version

- **Category**: Node API - Sui (JSON-RPC) / Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_tryGetPastObject

## Supported Chains
sui

## Method
`sui_tryGetPastObject`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `object_id` | `ObjectID` | required | the ID of the queried object |
| `version` | `SequenceNumber2` | required | the version of the queried object. If None, default to the latest known version |
| `options` | `ObjectDataOptions` | optional | options for specifying the content to be returned |

## Returns
`ObjectRead` - SuiPastObjectResponse

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_tryGetPastObject",
  "params": [
    "0x2",
    "4"
  ]
}
```
