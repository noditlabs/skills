# sui-sui_getNormalizedMoveModulesByPackage

> sui_getNormalizedMoveModulesByPackage

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getNormalizedMoveModulesByPackage

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_getNormalizedMoveModulesByPackage`

## Parameters

Array of parameters:

1. **package** (`any` (required)): The package ID

## Returns

An object. 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getNormalizedMoveModulesByPackage",
  "params": [
    "0x61630d3505f8905a0f4d42c6ff39a78a6ba2b28f68a3299ec3417bbabc6717dc"
  ]
}
```
