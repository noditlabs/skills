# sui-sui_getNormalizedMoveFunction

> sui_getNormalizedMoveFunction

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_getNormalizedMoveFunction`

## Parameters

Array of parameters:

1. **package** (`any` (required)): The package ID
2. **module_name** (`string` (required)): The module name
3. **function_name** (`string` (required)): The function name

## Returns

An object containing:
- `isEntry` (boolean): 
- `parameters` (array): 
- `return` (array): 
- `typeParameters` (array): 
- `visibility` (string): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getNormalizedMoveFunction",
  "params": [
    "0x9c4eb6769ca8b6a23efeb7298cf0a8d0b837b78749c2cfc711c42036cc6b7621",
    "moduleName",
    "functionName"
  ]
}
```
