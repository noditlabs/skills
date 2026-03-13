# sui-suix_getTotalSupply

> Returns the total supply of a specified coin type.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getTotalSupply

## Supported Chains
sui (mainnet)

## Method
`suix_getTotalSupply`

## Parameters
Array of 1 item:

1. **coin_type** (`string`, required): The fully qualified type name of the coin (e.g., `"0x2::sui::SUI"`).

## Returns
- **Supply** (`object`): The total supply information.
  - `value` (`string`): The total supply as a string-encoded u64 value.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getTotalSupply",
  "params": [
    "0x2::sui::SUI"
  ]
}
```
