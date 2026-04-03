# solana-getEpochInfo

> getEpochInfo

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getEpochInfo`

## Parameters

Array of parameters:

1. **Configuration Object** (`object` (required)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `minContextSlot` (string): The minimum slot at which the request can be evaluated.

## Returns

An object containing:
- `absoluteSlot` (integer): The current slot
- `blockHeight` (integer): The current block height
- `epoch` (integer): The current epoch
- `slotIndex` (integer): The current slot relative to the start of the current epoch
- `slotsInEpoch` (integer): The number of slots in this epoch
- `transactionCount` (integer): Total number of transactions processed without error since genesis

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getEpochInfo",
  "params": [
    {
      "commitment": "finalized"
    }
  ]
}
```
