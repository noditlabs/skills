# solana-getSlotLeader

> Returns the current slot leader

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getSlotLeader

## Supported Chains
solana (mainnet, devnet)

## Method
`getSlotLeader`

## Parameters
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.

## Returns
A string: Node identity Pubkey as base-58 encoded string.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getSlotLeader",
  "params": [{ "commitment": "finalized" }]
}
```
