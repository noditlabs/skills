# sui-suix_getReferenceGasPrice

> Returns the reference gas price for the current epoch used to calculate transaction gas costs.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getReferenceGasPrice

## Supported Chains
sui (mainnet)

## Method
`suix_getReferenceGasPrice`

## Parameters
None. This method takes no parameters.

## Returns
- **result** (`string`): The reference gas price as a string-encoded u64 value (in MIST, where 1 SUI = 10^9 MIST).

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getReferenceGasPrice",
  "params": []
}
```
