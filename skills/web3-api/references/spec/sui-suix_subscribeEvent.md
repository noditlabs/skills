# sui-suix_subscribeEvent

> Subscribe to a stream of Sui events matching the given filter via WebSocket. This is a WebSocket-only method.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_subscribeEvent

## Supported Chains
sui (mainnet)

## Method
`suix_subscribeEvent`

## Parameters
Array of 1 item:

1. **filter** (`object`, required): The event filter to subscribe to. Options include:
   - `MoveModule` (`object`): Filter by Move module — `{ "package": "<package_id>", "module": "<module_name>" }`.
   - `MoveEventType` (`string`): Filter by Move event type string.
   - `MoveEventModule` (`object`): Filter by the module that defined the event.
   - `MoveEventField` (`object`): Filter by a specific field path and value.
   - `Sender` (`string`): Filter by transaction sender address.
   - `Transaction` (`string`): Filter by transaction digest.
   - `TimeRange` (`object`): Filter by time range — `{ "startTime": "<ms>", "endTime": "<ms>" }`.
   - `All` (`array`): Match all conditions.
   - `Any` (`array`): Match any condition.

## Returns
Sends `SuiEvent` objects as notifications over the WebSocket connection:
- `id` (`object`): Event ID with `txDigest` and `eventSeq`.
- `packageId` (`string`): The package that emitted the event.
- `transactionModule` (`string`): The module that emitted the event.
- `sender` (`string`): The sender of the transaction.
- `type` (`string`): The event type.
- `parsedJson` (`object`): The event data parsed as JSON.
- `bcs` (`string`): BCS-encoded event data.
- `timestampMs` (`string`): Timestamp in milliseconds.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_subscribeEvent",
  "params": [
    {
      "MoveEventType": "0x2::coin::CoinEvent"
    }
  ]
}
```
