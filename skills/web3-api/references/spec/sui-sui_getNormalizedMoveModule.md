# sui-sui_getNormalizedMoveModule

> Return a structured representation of Move module

- **Category**: Node API - Sui (JSON-RPC) / Move Utils
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getNormalizedMoveModule

## Supported Chains
sui

## Method
`sui_getNormalizedMoveModule`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `package` | `ObjectID` | required |  |
| `module_name` | `string` | required |  |

## Returns
`SuiMoveNormalizedModule` - SuiMoveNormalizedModule

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getNormalizedMoveModule",
  "params": [
    "0x2",
    "example_string"
  ]
}
```
