# sui-suix_getTotalSupply

> suix_getTotalSupply

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getTotalSupply`

## Parameters

Array of parameters:

1. **coin_type** (`string` (required)): Type name for the coin (e.g., 0x168da5bf1f48dafc111b0a488fa454aca95e0b5e::usdc::USDC)

## Returns

An object containing:
- `value` (string): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getTotalSupply",
  "params": [
    "0xe5c651321915b06c81838c2e370109b554a448a78d3a56220f798398dde66eab::acoin::ACOIN"
  ]
}
```
