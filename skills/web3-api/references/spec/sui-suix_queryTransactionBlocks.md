# sui-suix_queryTransactionBlocks

> Returns a list of transaction blocks matching the specified query criteria, with pagination and ordering support.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_queryTransactionBlocks

## Supported Chains
sui (mainnet)

## Method
`suix_queryTransactionBlocks`

## Parameters
Array of 4 items:

1. **query** (`object`, required): The transaction block query filter.
   - `filter` (`object` | `null`): Filter criteria. Options include:
     - `Checkpoint` (`string`): Filter by checkpoint sequence number.
     - `MoveFunction` (`object`): Filter by Move function — `{ "package": "<id>", "module": "<name>", "function": "<name>" }`.
     - `InputObject` (`string`): Filter by input object ID.
     - `ChangedObject` (`string`): Filter by changed object ID.
     - `FromAddress` (`string`): Filter by sender address.
     - `ToAddress` (`string`): Filter by recipient address.
     - `FromAndToAddress` (`object`): Filter by both sender and recipient — `{ "from": "<addr>", "to": "<addr>" }`.
     - `TransactionKind` (`string`): Filter by transaction kind (e.g., `"ProgrammableTransaction"`).
   - `options` (`object` | `null`): Options to control what data to return.
     - `showInput` (`boolean`): Include transaction input data.
     - `showRawInput` (`boolean`): Include raw transaction input.
     - `showEffects` (`boolean`): Include transaction effects.
     - `showEvents` (`boolean`): Include events emitted.
     - `showObjectChanges` (`boolean`): Include object changes.
     - `showBalanceChanges` (`boolean`): Include balance changes.
     - `showRawEffects` (`boolean`): Include raw effects.

2. **cursor** (`string` | `null`, optional): Paging cursor (transaction digest). Default: `null`.

3. **limit** (`integer` | `null`, optional): Maximum number of items per page.

4. **descending_order** (`boolean`, optional): If `true`, results are returned in descending order. Default: `false`.

## Returns
- **TransactionBlocksPage** (`object`): Paginated list of transaction blocks.
  - `data` (`array`): Array of `SuiTransactionBlockResponse` objects.
  - `nextCursor` (`string` | `null`): Cursor for the next page.
  - `hasNextPage` (`boolean`): Whether more results are available.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_queryTransactionBlocks",
  "params": [
    {
      "filter": {
        "FromAddress": "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3"
      },
      "options": {
        "showInput": true,
        "showEffects": true,
        "showEvents": true
      }
    },
    null,
    10,
    true
  ]
}
```
