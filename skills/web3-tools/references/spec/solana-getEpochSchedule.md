# solana-getEpochSchedule

> getEpochSchedule

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getEpochSchedule

## Supported Chains

Solana (mainnet, devnet)

## Method

`getEpochSchedule`

## Parameters

None - this method takes no parameters.

## Returns

An object containing:
- `firstNormalEpoch` (integer): First normal-length epoch, log2(slotsPerEpoch) - log2(MINIMUM_SLOTS_PER_EPOCH)
- `firstNormalSlot` (integer): Minimum number of slots in an epoch, MINIMUM_SLOTS_PER_EPOCH * (2.pow(firstNormalEpoch) - 1)
- `leaderScheduleSlotOffset` (integer): The number of slots before beginning of an epoch to calculate a leader schedule for that epoch.
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
