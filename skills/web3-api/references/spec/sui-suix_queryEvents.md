# sui-suix_queryEvents

> Returns a list of events matching the specified query criteria, with pagination and ordering support.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_queryEvents

## Supported Chains
sui (mainnet)

## Method
`suix_queryEvents`

## Parameters
Array of 4 items:

1. **query** (`object`, required): The event query filter. Options include:
   - `MoveModule` (`object`): Filter by Move module — `{ "package": "<package_id>", "module": "<module_name>" }`.
   - `MoveEventType` (`string`): Filter by Move event type string.
   - `MoveEventModule` (`object`): Filter by the module that defined the event type.
   - `MoveEventField` (`object`): Filter by a specific field path and value in the event.
   - `Sender` (`string`): Filter by transaction sender address.
   - `Transaction` (`string`): Filter by transaction digest.
   - `TimeRange` (`object`): Filter by time range — `{ "startTime": "<ms>", "endTime": "<ms>" }`.
   - `All` (`array`): Match all conditions.
   - `Any` (`array`): Match any condition.

2. **cursor** (`object` | `null`, optional): Paging cursor with `txDigest` and `eventSeq` fields. Default: `null`.

3. **limit** (`integer` | `null`, optional): Maximum number of items per page.

4. **descending_order** (`boolean`, optional): If `true`, results are returned in descending order. Default: `false`.

## Returns
- **EventPage** (`object`): Paginated list of events.
  - `data` (`array`): Array of `SuiEvent` objects.
    - `id` (`object`): Event ID with `txDigest` and `eventSeq`.
    - `packageId` (`string`): The package that emitted the event.
    - `transactionModule` (`string`): The module that emitted the event.
    - `sender` (`string`): The sender of the transaction.
    - `type` (`string`): The event type.
    - `parsedJson` (`object`): The event data parsed as JSON.
    - `bcs` (`string`): BCS-encoded event data.
    - `timestampMs` (`string`): Timestamp in milliseconds.
  - `nextCursor` (`object` | `null`): Cursor for the next page.
  - `hasNextPage` (`boolean`): Whether more results are available.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_queryEvents",
  "params": [
    {
      "MoveModule": {
        "package": "0x2",
        "module": "coin"
      }
    },
    null,
    10,
    false
  ]
}
```
