# sui-sui_getProtocolConfig

> sui_getProtocolConfig

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_getProtocolConfig`

## Parameters

Array of parameters:

1. **version** (`any` (optional)): An optional protocol version specifier. If omitted, the latest protocol config table for the node will be returned.

## Returns

An object containing:
- `attributes` (object): 
- `featureFlags` (object): 
- `maxSupportedProtocolVersion` (string): 
- `minSupportedProtocolVersion` (string): 
- `protocolVersion` (string): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getProtocolConfig",
  "params": [
    6
  ]
}
```
