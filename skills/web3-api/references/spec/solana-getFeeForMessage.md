# solana-getFeeForMessage

> Get the fee the network will charge for a particular Message

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getFeeForMessage

## Supported Chains
solana (mainnet, devnet)

## Method
`getFeeForMessage`

## Parameters
- **Message** (string, required): Base-64 encoded Message.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (integer): Fee corresponding to the message at the specified blockhash (uint64).

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getFeeForMessage",
  "params": [
    "AQABAgIAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAEBAQAA",
    { "commitment": "processed" }
  ]
}
```
