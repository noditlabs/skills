# solana-getBlocksWithLimit

> Returns a list of confirmed blocks starting at the given slot

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBlocksWithLimit

## Supported Chains
solana (mainnet, devnet)

## Method
`getBlocksWithLimit`

## Parameters
- **Start slot** (integer, required): The start slot number (uint64).
- **Limit** (integer, required): Limit, must be no more than 500,000 blocks higher than the start_slot (uint64).
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.

## Returns
An array of u64 integers listing confirmed blocks starting at start_slot for up to limit blocks, inclusive.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlocksWithLimit",
  "params": [338967300, 10]
}
```
