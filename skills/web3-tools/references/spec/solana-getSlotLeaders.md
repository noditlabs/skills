# solana-getSlotLeaders

> getSlotLeaders

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getSlotLeaders`

## Parameters

Array of parameters:

1. **StartSlot** (`any` (required)): 
2. **Limit** (`integer` (required)): The limit of the result. It must be between 1 and 500000.

## Returns

An array of objects. Array of Node identity public keys as base-58 encoded strings.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getSlotLeaders",
  "params": [
    100,
    10
  ]
}
```
