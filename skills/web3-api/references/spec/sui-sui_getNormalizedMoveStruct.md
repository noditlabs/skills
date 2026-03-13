# sui-sui_getNormalizedMoveStruct

> Return a structured representation of Move struct

- **Category**: Node API - Sui (JSON-RPC) / Move Utils
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getNormalizedMoveStruct

## Supported Chains
sui

## Method
`sui_getNormalizedMoveStruct`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `package` | `ObjectID` | required |  |
| `module_name` | `string` | required |  |
| `struct_name` | `string` | required |  |

## Returns
`SuiMoveNormalizedStruct` - SuiMoveNormalizedStruct

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getNormalizedMoveStruct",
  "params": [
    "0x2",
    "example_string",
    "example_string"
  ]
}
```
