# sui-suix_getDynamicFields

> Returns the list of dynamic field objects owned by a specified object, with pagination support.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getDynamicFields

## Supported Chains
sui (mainnet)

## Method
`suix_getDynamicFields`

## Parameters
Array of 3 items:

1. **parent_object_id** (`string`, required): The ID of the parent object to query dynamic fields for.

2. **cursor** (`string` | `null`, optional): An optional paging cursor. If provided, the query will start from the next item after the specified cursor. Default: `null`.

3. **limit** (`integer` | `null`, optional): Maximum number of items per page. Default: `null` (server default applies).

## Returns
- **DynamicFieldPage** (`object`): A paginated list of dynamic fields.
  - `data` (`array`): Array of dynamic field info objects.
    - `name` (`object`): The dynamic field name with `type` and `value`.
    - `bcsName` (`string`): BCS-encoded name.
    - `type` (`string`): Either `"DynamicField"` or `"DynamicObject"`.
    - `objectType` (`string`): The type of the dynamic field object.
    - `objectId` (`string`): The object ID of the dynamic field.
    - `version` (`integer`): The version of the dynamic field object.
    - `digest` (`string`): The digest of the dynamic field object.
  - `nextCursor` (`string` | `null`): Cursor for the next page, or `null` if no more results.
  - `hasNextPage` (`boolean`): Whether more results are available.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getDynamicFields",
  "params": [
    "0x5c890d6e7bfa66e51b56744599545e5c1733fda3cc1e44e0413b62e0e6774cbd",
    null,
    10
  ]
}
```
