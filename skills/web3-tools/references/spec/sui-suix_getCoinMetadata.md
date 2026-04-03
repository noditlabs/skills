# sui-suix_getCoinMetadata

> suix_getCoinMetadata

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getCoinMetadata`

## Parameters

Array of parameters:

1. **coin_type** (`string` (required)): Type name for the coin (e.g., 0x168da5bf1f48dafc111b0a488fa454aca95e0b5e::usdc::USDC)

## Returns

An object containing:
- `decimals` (integer): Number of decimal places the coin uses.
- `description` (string): Description of the token
- `iconUrl` (['string', 'null']): URL for the token logo
- `id` (string): hexadecimal string encoding.
- `name` (string): Name for the token
- `symbol` (string): Symbol for the token

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getCoinMetadata",
  "params": [
    "0x168da5bf1f48dafc111b0a488fa454aca95e0b5e::usdc::USDC"
  ]
}
```
