# sui-sui_getObject

> Return the object information for a specified object

- **Category**: Node API - Sui (JSON-RPC) / Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getObject

## Supported Chains
sui

## Method
`sui_getObject`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `object_id` | `ObjectID` | required | the ID of the queried object |
| `options` | `ObjectDataOptions` | optional | options for specifying the content to be returned |

## Returns
`SuiObjectResponse` - SuiObjectResponse

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getObject",
  "params": [
    "0x2"
  ]
}
```
