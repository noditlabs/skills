# sui-suix_getBalance

> suix_getBalance

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getBalance`

## Parameters

Array of parameters:

1. **owner** (`any` (required)): Sui address.
2. **coin_type** (`string` (optional)): ( : 0x168da5bf1f48dafc111b0a488fa454aca95e0b5e::usdc::USDC). 0x2::sui::SUI value.

## Returns

An object containing:
- `coinObjectCount` (integer): 
- `coinType` (string): 
- `lockedBalance` (object): 
- `totalBalance` (string): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getBalance",
  "params": [
    "0xa6f5a7953a75dc632e696cabe60560522a017bf2fb0bd930d1ec22c06f1ee4e4",
    "0x168da5bf1f48dafc111b0a488fa454aca95e0b5e::usdc::USDC"
  ]
}
```
