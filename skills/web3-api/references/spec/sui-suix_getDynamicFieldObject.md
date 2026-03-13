# sui-suix_getDynamicFieldObject

> Returns the dynamic field object information for a specified parent object and dynamic field name.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getDynamicFieldObject

## Supported Chains
sui (mainnet)

## Method
`suix_getDynamicFieldObject`

## Parameters
Array of 2 items:

1. **parent_object_id** (`string`, required): The ID of the parent object that owns the dynamic field.

2. **name** (`object`, required): The dynamic field name object.
   - `type` (`string`, required): The type of the dynamic field name (e.g., `"u64"`, `"address"`, `"0x2::object::ID"`).
   - `value` (`string`, required): The value of the dynamic field name.

## Returns
- **SuiObjectResponse** (`object`): The object data for the dynamic field.
  - `data` (`object` | `null`): Object data including `objectId`, `version`, `digest`, `type`, `owner`, `content`, etc.
  - `error` (`object` | `null`): Error info if the object could not be retrieved.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getDynamicFieldObject",
  "params": [
    "0x5c890d6e7bfa66e51b56744599545e5c1733fda3cc1e44e0413b62e0e6774cbd",
    {
      "type": "u64",
      "value": "1"
    }
  ]
}
```
