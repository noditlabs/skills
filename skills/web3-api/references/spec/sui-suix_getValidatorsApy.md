# sui-suix_getValidatorsApy

> Returns the APY (Annual Percentage Yield) for all active validators in the current epoch.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getValidatorsApy

## Supported Chains
sui (mainnet)

## Method
`suix_getValidatorsApy`

## Parameters
None. This method takes no parameters.

## Returns
- **ValidatorsApy** (`object`): APY data for validators.
  - `epoch` (`string`): The current epoch number.
  - `apys` (`array`): Array of validator APY entries.
    - `address` (`string`): The validator's Sui address.
    - `apy` (`number`): The annual percentage yield as a decimal (e.g., 0.05 = 5%).

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getValidatorsApy",
  "params": []
}
```
