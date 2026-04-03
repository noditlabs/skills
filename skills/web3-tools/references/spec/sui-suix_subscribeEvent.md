# sui-suix_subscribeEvent

> suix_subscribeEvent

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_subscribeEvent`

## Parameters

Array of parameters:

1. **filter** (`any` (required)): The filter criteria of the event stream. See Event filter documentation for examples.

## Returns

An object containing:
- `id` (object): Unique ID of a Sui Event, the ID is a combination of transaction digest and event seq number.
- `packageId` (object): 
- `parsedJson` (any): Parsed json value of the event
- `sender` (object): 
- `timestampMs` (string): 
- `transactionModule` (string): Move module where this event was emitted.
- `type` (string): Move event type.

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "suix_subscribeEvent"
}
```
