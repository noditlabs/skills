# solana-getBlockProduction

> Returns recent block production information from the current or previous epoch

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBlockProduction

## Supported Chains
solana (mainnet, devnet)

## Method
`getBlockProduction`

## Parameters
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `identity` (string): Only return results for this validator identity (base-58 encoded).
  - `range` (object): Slot range to return block production for. Defaults to current epoch.
    - `firstSlot` (integer, required): First slot to return block production information for (inclusive).
    - `lastSlot` (integer): Last slot to return block production information for (inclusive).

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (object): Block production information by validator identity.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlockProduction",
  "params": [{
    "commitment": "finalized",
    "identity": "12i8gndWWWMTRzJBFhnYkobNgZB3XMUUJq75HeUrshrk",
    "range": { "firstSlot": 363067597, "lastSlot": 364115359 }
  }]
}
```
