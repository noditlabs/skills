# sui-suix_getLatestSuiSystemState

> suix_getLatestSuiSystemState

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getLatestSuiSystemState

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getLatestSuiSystemState`

## Parameters

None - this method takes no parameters.

## Returns

An object containing:
- `activeValidators` (array): The list of active validators in the current epoch.
- `atRiskValidators` (array): Map storing the number of epochs for which each validator has been below the low stake threshold.
- `epoch` (string): 
- `epochDurationMs` (string): 
- `epochStartTimestampMs` (string): 
- `inactivePoolsId` (object): 
- `inactivePoolsSize` (string): 
- `maxValidatorCount` (string): 
- `minValidatorJoiningStake` (string): 
- `pendingActiveValidatorsId` (object): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getLatestSuiSystemState",
  "params": []
}
```
