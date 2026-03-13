# sui-sui_getNormalizedMoveFunction

> Return a structured representation of Move function

- **Category**: Node API - Sui (JSON-RPC) / Move Utils
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getNormalizedMoveFunction

## Supported Chains
sui

## Method
`sui_getNormalizedMoveFunction`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `package` | `ObjectID` | required |  |
| `module_name` | `string` | required |  |
| `function_name` | `string` | required |  |

## Returns
`SuiMoveNormalizedFunction` - SuiMoveNormalizedFunction

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getNormalizedMoveFunction",
  "params": [
    "0x2",
    "example_string",
    "example_string"
  ]
}
```
