# sui-suix_getAllCoins

> suix_getAllCoins

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getAllCoins`

## Parameters

Array of parameters:

1. **owner** (`any` (required)): Sui address.
2. **cursor** (`string` (optional)): Optional paging cursor
3. **limit** (`integer` (optional)): Maximum number of items per page

## Returns

An object containing:
- `data` (array): 
- `hasNextPage` (boolean): 
- `nextCursor` (['string', 'null']): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getAllCoins",
  "params": [
    "0x41f5975e3c6bd5c95f041a8493ad7e9934be26e69152d2c2e86d8a9bdbd242b3",
    "0x2564cd31a71cf9833609b111436d8f0f47b7f8b9927ec3f8975a1dcbf9b25564",
    3
  ]
}
```
