# sui-sui_getNormalizedMoveModulesByPackage

> Return structured representations of all modules in the given package

- **Category**: Node API - Sui (JSON-RPC) / Move Utils
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getNormalizedMoveModulesByPackage

## Supported Chains
sui

## Method
`sui_getNormalizedMoveModulesByPackage`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `package` | `ObjectID` | required |  |

## Returns
`object` - BTreeMap<String,SuiMoveNormalizedModule>

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getNormalizedMoveModulesByPackage",
  "params": [
    "0x2"
  ]
}
```
