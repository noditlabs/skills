# sui-sui_getMoveFunctionArgTypes

> sui_getMoveFunctionArgTypes

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_getMoveFunctionArgTypes`

## Parameters

Array of parameters:

1. **package** (`any` (required)): The package ID
2. **module** (`string` (required)): The module name
3. **function** (`string` (required)): The function name

## Returns

An array of objects. 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getMoveFunctionArgTypes",
  "params": [
    "0xa0a7b108f5023b7356f2c6a4be6f058e267aae38e08260c7d519d8641897490c",
    "suifrens",
    "mint"
  ]
}
```
