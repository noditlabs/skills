# sui-sui_getNormalizedMoveModule

> sui_getNormalizedMoveModule

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getNormalizedMoveModule

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_getNormalizedMoveModule`

## Parameters

Array of parameters:

1. **package** (`any` (required)): The package ID
2. **module_name** (`string` (required)): The module name

## Returns

An object containing:
- `address` (string): 
- `enums` (object): 
- `exposedFunctions` (object): 
- `fileFormatVersion` (integer): 
- `friends` (array): 
- `name` (string): 
- `structs` (object): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getNormalizedMoveModule",
  "params": [
    "0x0047d5fa0a823e7d0ff4d55c32b09995a0ae1eedfee9c7b1354e805ed10ee3d0",
    "module"
  ]
}
```
