# sui-suix_getOwnedObjects

> Returns the list of objects owned by a specified address. For large result sets exceeding QUERY_MAX_RESULT_LIMIT, use suix_queryObjects for better pagination accuracy.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getOwnedObjects

## Supported Chains
sui (mainnet)

## Method
`suix_getOwnedObjects`

## Parameters
Array of 4 items:

1. **address** (`string`, required): The owner's Sui address to query objects for.

2. **query** (`object` | `null`, optional): Optional query filter to narrow results.
   - `filter` (`object` | `null`): Filter criteria. Options include:
     - `MatchAll` (`array`): All conditions must match.
     - `MatchAny` (`array`): Any condition can match.
     - `MatchNone` (`array`): None of the conditions should match.
     - `Package` (`string`): Filter by package ID.
     - `MoveModule` (`object`): Filter by module with `package` and `module` fields.
     - `StructType` (`string`): Filter by struct type.
     - `AddressOwner` (`string`): Filter by address owner.
     - `ObjectOwner` (`string`): Filter by object owner.
     - `ObjectId` (`string`): Filter by object ID.
     - `ObjectIds` (`array`): Filter by multiple object IDs.
     - `Version` (`string`): Filter by version.
   - `options` (`object` | `null`): Options to control what data to return.
     - `showType` (`boolean`): Include the object type.
     - `showOwner` (`boolean`): Include owner info.
     - `showPreviousTransaction` (`boolean`): Include previous transaction digest.
     - `showDisplay` (`boolean`): Include display metadata.
     - `showContent` (`boolean`): Include object content.
     - `showBcs` (`boolean`): Include BCS bytes.
     - `showStorageRebate` (`boolean`): Include storage rebate info.

3. **cursor** (`string` | `null`, optional): Paging cursor. If provided, query starts after this object ID.

4. **limit** (`integer` | `null`, optional): Maximum number of items per page.

## Returns
- **PaginatedObjectsResponse** (`object`): Paginated list of owned objects.
  - `data` (`array`): Array of `SuiObjectResponse` objects.
  - `nextCursor` (`string` | `null`): Cursor for the next page.
  - `hasNextPage` (`boolean`): Whether more results are available.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getOwnedObjects",
  "params": [
    "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3",
    {
      "filter": {
        "StructType": "0x2::coin::Coin<0x2::sui::SUI>"
      },
      "options": {
        "showType": true,
        "showContent": true,
        "showOwner": true
      }
    },
    null,
    10
  ]
}
```
