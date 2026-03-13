# sui-sui_getMoveFunctionArgTypes

> Return the argument types of a Move function, based on normalized Type.

- **Category**: Node API - Sui (JSON-RPC) / Move Utils
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getMoveFunctionArgTypes

## Supported Chains
sui

## Method
`sui_getMoveFunctionArgTypes`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `package` | `ObjectID` | required |  |
| `module` | `string` | required |  |
| `function` | `string` | required |  |

## Returns
`array` - Vec<MoveFunctionArgType>

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getMoveFunctionArgTypes",
  "params": [
    "0x2",
    "example_string",
    "example_string"
  ]
}
```
