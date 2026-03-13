# solana-getLatestBlockhash

> Returns the latest blockhash

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getLatestBlockhash

## Supported Chains
solana (mainnet, devnet)

## Method
`getLatestBlockhash`

## Parameters
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (object):
  - `blockhash` (string): The blockhash of the block, as base-58 encoded string.
  - `lastValidBlockHeight` (integer): Last block height at which the blockhash will be valid.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getLatestBlockhash",
  "params": [{ "commitment": "processed" }]
}
```
