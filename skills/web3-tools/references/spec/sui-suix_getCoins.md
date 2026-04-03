# sui-suix_getCoins

> suix_getCoins

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getCoins`

## Parameters

Array of parameters:

1. **owner** (`any` (required)): Sui address.
2. **coin_type** (`string` (optional)): Optional type name for the coin (e.g., 0x168da5bf1f48dafc111b0a488fa454aca95e0b5e::usdc::USDC), default to 0x2::sui::SUI if not specified.
3. **cursor** (`string` (optional)): Optional paging cursor
4. **limit** (`integer` (optional)): Maximum number of items per page

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
  "method": "suix_getCoins",
  "params": [
    "0x6d907beaa3a49db57bdfdb3557e6d405cbf01c293a53e01457d65e92b5d8dd68",
    "0x2::sui::SUI",
    "0xee6b5173afedb35330f60397c2cbb48196ba41921246c304be7b490cee0904eb",
    3
  ]
}
```
