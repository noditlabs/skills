# solana-getEpochSchedule

> Returns the epoch schedule information from this cluster

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getEpochSchedule

## Supported Chains
solana (mainnet, devnet)

## Method
`getEpochSchedule`

## Parameters
None.

## Returns
An object containing:
- `firstNormalEpoch` (integer): First normal-length epoch.
- `firstNormalSlot` (integer): Minimum number of slots in an epoch.
- `leaderScheduleSlotOffset` (integer): The number of slots before beginning of an epoch to calculate a leader schedule.
- `slotsPerEpoch` (integer): The maximum number of slots in each epoch.
- `warmup` (boolean): Whether epochs start short and grow.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getEpochSchedule"
}
```
