# solana-getBlockTime

> getBlockTime

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getBlockTime`

## Parameters

Array of parameters:

1. **Block number** (`any` (required)): 

## Returns

- **result**: Estimated production time, as Unix timestamp (seconds since the Unix epoch) | object

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlockTime",
  "params": [
    338967300
  ]
}
```
