# solana-getLatestBlockhash

> getLatestBlockhash

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getLatestBlockhash

## Supported Chains

Solana (mainnet, devnet)

## Method

`getLatestBlockhash`

## Parameters

Array of 0-1 item(s). . 1. Configuration Object ( )

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (object): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getLatestBlockhash",
  "params": [
    {
      "commitment": "processed"
    }
  ]
}
```
