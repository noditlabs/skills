# solana-getInflationRate

> Returns the specific inflation values for the current epoch

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getInflationRate

## Supported Chains
solana (mainnet, devnet)

## Method
`getInflationRate`

## Parameters
None.

## Returns
An object containing:
- `total` (number): Total inflation.
- `validator` (number): Inflation allocated to validators.
- `foundation` (number): Inflation allocated to the foundation.
- `epoch` (integer): Epoch for which these values are valid.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getInflationRate"
}
```
