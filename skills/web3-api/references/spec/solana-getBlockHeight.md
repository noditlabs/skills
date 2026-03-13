# solana-getBlockHeight

> Returns the current block height of the node

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBlockHeight

## Supported Chains
solana (mainnet, devnet)

## Method
`getBlockHeight`

## Parameters
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.

## Returns
An integer representing the current block height.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlockHeight",
  "params": [{ "commitment": "finalized" }]
}
```
