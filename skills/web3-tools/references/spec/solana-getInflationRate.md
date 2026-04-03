# solana-getInflationRate

> getInflationRate

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getInflationRate`

## Parameters

None - this method takes no parameters.

## Returns

An object containing:
- `total` (number): Total inflation
- `validator` (number): Inflation allocated to validators
- `foundation` (number): Inflation allocated to the foundation
- `epoch` (integer): Epoch for which these values are valid

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getInflationRate"
}
```
