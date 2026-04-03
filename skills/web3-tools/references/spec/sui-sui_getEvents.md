# sui-sui_getEvents

> sui_getEvents

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_getEvents`

## Parameters

Array of parameters:

1. **transaction_digest** (`any` (required)): The event query criteria

## Returns

An array of objects. 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getEvents",
  "params": [
    "11a72GCQ5hGNpWGh2QhQkkusTEGS6EDqifJqxr7nSYX"
  ]
}
```
