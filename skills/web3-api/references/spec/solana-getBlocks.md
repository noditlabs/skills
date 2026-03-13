# solana-getBlocks

> Returns a list of confirmed blocks between two slots

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBlocks

## Supported Chains
solana (mainnet, devnet)

## Method
`getBlocks`

## Parameters
- **Start slot** (integer, required): The start slot number (uint64).
- **End slot** (integer, optional): The end slot number (uint64).
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.

## Returns
An array of u64 integers listing confirmed blocks between start_slot and either end_slot (if provided) or latest confirmed slot, inclusive. Max range allowed is 500,000 slots.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlocks",
  "params": [338967300, 338967310, { "commitment": "finalized" }]
}
```
