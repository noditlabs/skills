# sui-suix_getStakesByIds

> Returns one or more DelegatedStake objects by their StakedSui object IDs. If a stake has been withdrawn, its status is Unstaked.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getStakesByIds

## Supported Chains
sui (mainnet)

## Method
`suix_getStakesByIds`

## Parameters
Array of 1 item:

1. **staked_sui_ids** (`array` of `string`, required): An array of StakedSui object IDs to query.

## Returns
- **result** (`array`): Array of `DelegatedStake` objects.
  - `validatorAddress` (`string`): The validator's Sui address.
  - `stakingPool` (`string`): The staking pool object ID.
  - `stakes` (`array`): Array of individual stake objects.
    - `stakedSuiId` (`string`): The StakedSui object ID.
    - `stakeRequestEpoch` (`string`): Epoch when the stake was requested.
    - `stakeActiveEpoch` (`string`): Epoch when the stake became active.
    - `principal` (`string`): The staked amount in MIST.
    - `status` (`string`): Stake status — `"Active"`, `"Pending"`, or `"Unstaked"`.
    - `estimatedReward` (`string` | `null`): Estimated reward in MIST.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getStakesByIds",
  "params": [
    [
      "0xa1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0",
      "0xf0e1d2c3b4a5f6e7d8c9b0a1f2e3d4c5b6a7f8e9"
    ]
  ]
}
```
