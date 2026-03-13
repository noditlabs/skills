# sui-suix_subscribeTransaction

> Subscribe to a stream of transactions matching the given filter via WebSocket. This is a WebSocket-only method.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_subscribeTransaction

## Supported Chains
sui (mainnet)

## Method
`suix_subscribeTransaction`

## Parameters
Array of 1 item:

1. **filter** (`object`, required): The transaction filter to subscribe to. Options include:
   - `Checkpoint` (`string`): Filter by checkpoint sequence number.
   - `MoveFunction` (`object`): Filter by Move function — `{ "package": "<id>", "module": "<name>", "function": "<name>" }`.
   - `InputObject` (`string`): Filter by input object ID.
   - `ChangedObject` (`string`): Filter by changed object ID.
   - `FromAddress` (`string`): Filter by sender address.
   - `ToAddress` (`string`): Filter by recipient address.
   - `FromAndToAddress` (`object`): Filter by both sender and recipient — `{ "from": "<addr>", "to": "<addr>" }`.
   - `TransactionKind` (`string`): Filter by transaction kind (e.g., `"ProgrammableTransaction"`).

## Returns
Sends `SuiTransactionBlockEffects` objects as notifications over the WebSocket connection, containing transaction execution results including status, gas usage, created/mutated/deleted objects, and events.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_subscribeTransaction",
  "params": [
    {
      "FromAddress": "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3"
    }
  ]
}
```
