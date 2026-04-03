# sui-suix_resolveNameServiceAddress

> suix_resolveNameServiceAddress

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_resolveNameServiceAddress`

## Parameters

Array of parameters:

1. **name** (`string` (required)): The name to resolve

## Returns

- **result** (`string`): hexadecimal string encoding.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_resolveNameServiceAddress",
  "params": [
    "example.sui"
  ]
}
```
