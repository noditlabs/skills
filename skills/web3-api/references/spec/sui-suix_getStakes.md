# sui-suix_getStakes

> Returns all DelegatedStake objects for a specified owner address.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getStakes

## Supported Chains
sui (mainnet)

## Method
`suix_getStakes`

## Parameters
Array of 1 item:

1. **owner** (`string`, required): The owner's Sui address to query stakes for.

## Returns
- **result** (`array`): Array of `DelegatedStake` objects.
  - `validatorAddress` (`string`): The validator's Sui address.
  - `stakingPool` (`string`): The staking pool object ID.
  - `stakes` (`array`): Array of individual stake objects.
    - `stakedSuiId` (`string`): The StakedSui object ID.
    - `stakeRequestEpoch` (`string`): Epoch when the stake was requested.
    - `stakeActiveEpoch` (`string`): Epoch when the stake became active.
    - `principal` (`string`): The staked amount in MIST.
    - `status` (`string`): Stake status — `"Active"` or `"Pending"` with optional estimated reward.
    - `estimatedReward` (`string` | `null`): Estimated reward in MIST (only for active stakes).

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getStakes",
  "params": [
    "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3"
  ]
}
```
