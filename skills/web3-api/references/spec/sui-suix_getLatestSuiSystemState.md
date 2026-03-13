# sui-suix_getLatestSuiSystemState

> Returns the latest on-chain SUI system state object containing validator set, epoch, and protocol configuration info.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getLatestSuiSystemState

## Supported Chains
sui (mainnet)

## Method
`suix_getLatestSuiSystemState`

## Parameters
None. This method takes no parameters.

## Returns
- **SuiSystemStateSummary** (`object`): The latest system state summary.
  - `epoch` (`string`): Current epoch number.
  - `protocolVersion` (`string`): Current protocol version.
  - `systemStateVersion` (`string`): System state version.
  - `storageFundTotalObjectStorageRebates` (`string`): Total storage rebates in the fund.
  - `storageFundNonRefundableBalance` (`string`): Non-refundable balance in storage fund.
  - `referenceGasPrice` (`string`): Reference gas price for the current epoch.
  - `safeMode` (`boolean`): Whether the system is in safe mode.
  - `epochStartTimestampMs` (`string`): Epoch start timestamp in milliseconds.
  - `epochDurationMs` (`string`): Duration of the epoch in milliseconds.
  - `stakeSubsidyStartEpoch` (`string`): Epoch when stake subsidy started.
  - `stakeSubsidyBalance` (`string`): Remaining stake subsidy balance.
  - `stakeSubsidyDistributionCounter` (`string`): Distribution counter.
  - `stakeSubsidyCurrentDistributionAmount` (`string`): Current distribution amount.
  - `stakeSubsidyPeriodLength` (`string`): Period length for subsidy distribution.
  - `stakeSubsidyDecreaseRate` (`integer`): Decrease rate for subsidy.
  - `totalStake` (`string`): Total amount staked in the network.
  - `activeValidators` (`array`): List of active validators with their metadata.
  - `pendingActiveValidatorsId` (`string`): ID of pending active validators table.
  - `pendingActiveValidatorsSize` (`string`): Size of pending active validators.
  - `pendingRemovals` (`array`): Indices of validators pending removal.
  - `stakingPoolMappingsId` (`string`): ID of staking pool mappings table.
  - `stakingPoolMappingsSize` (`string`): Size of staking pool mappings.
  - `inactivePoolsId` (`string`): ID of inactive pools table.
  - `inactivePoolsSize` (`string`): Size of inactive pools.
  - `validatorCandidatesId` (`string`): ID of validator candidates table.
  - `validatorCandidatesSize` (`string`): Size of validator candidates.
  - `maxValidatorCount` (`string`): Maximum validator count.
  - `minValidatorJoiningStake` (`string`): Minimum stake to join as validator.
  - `validatorLowStakeThreshold` (`string`): Low stake threshold for validators.
  - `validatorVeryLowStakeThreshold` (`string`): Very low stake threshold.
  - `validatorLowStakeGracePeriod` (`string`): Grace period for low stake validators.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getLatestSuiSystemState",
  "params": []
}
```
