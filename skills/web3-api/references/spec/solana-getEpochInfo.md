# solana-getEpochInfo

> Returns information about the current epoch

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getEpochInfo

## Supported Chains
solana (mainnet, devnet)

## Method
`getEpochInfo`

## Parameters
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.

## Returns
An object containing:
- `absoluteSlot` (integer): The current slot.
- `blockHeight` (integer): The current block height.
- `epoch` (integer): The current epoch.
- `slotIndex` (integer): The current slot relative to the start of the current epoch.
- `slotsInEpoch` (integer): The number of slots in this epoch.
- `transactionCount` (integer): Total number of transactions processed without error since genesis.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getEpochInfo",
  "params": [{ "commitment": "finalized" }]
}
```
