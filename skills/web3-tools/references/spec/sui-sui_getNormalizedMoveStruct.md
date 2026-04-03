# sui-sui_getNormalizedMoveStruct

> sui_getNormalizedMoveStruct

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_getNormalizedMoveStruct`

## Parameters

Array of parameters:

1. **package** (`any` (required)): The package ID
2. **module_name** (`string` (required)): The module name
3. **struct_name** (`string` (required)): The struct name

## Returns

An object containing:
- `abilities` (object): 
- `fields` (array): 
- `typeParameters` (array): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getNormalizedMoveStruct",
  "params": [
    "0xc95b9e341bc3aba1654bdbad707dcd773bd6309363447ef3fe58a960de92aa93",
    "module",
    "StructName"
  ]
}
```
