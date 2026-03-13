# solana-getSlot

> Returns the slot that has reached the given or default commitment level

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getSlot

## Supported Chains
solana (mainnet, devnet)

## Method
`getSlot`

## Parameters
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.

## Returns
An integer (uint64): Current slot.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getSlot",
  "params": [{ "commitment": "finalized" }]
}
```
