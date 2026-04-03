# solana-getFeeForMessage

> getFeeForMessage

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getFeeForMessage`

## Parameters

Array of parameters:

1. **Message** (`string` (required)): Base-64 encoded Message
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `minContextSlot` (string): The minimum slot at which the request can be evaluated.

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (integer): Fee corresponding to the message at the specified blockhash

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getFeeForMessage",
  "params": [
    "AQABAgIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAEBAQAA",
    {
      "commitment": "processed"
    }
  ]
}
```
