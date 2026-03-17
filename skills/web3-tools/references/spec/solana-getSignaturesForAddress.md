# solana-getSignaturesForAddress

> getSignaturesForAddress

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getSignaturesForAddress

## Supported Chains

Solana (mainnet, devnet)

## Method

`getSignaturesForAddress`

## Parameters

Array of 1-2 item(s). . 1. Account address ( ) 2. Configuration Object ( )

## Returns

An array of objects. 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getSignaturesForAddress",
  "params": [
    "Vote111111111111111111111111111111111111111",
    {
      "commitment": "finalized",
      "limit": 1
    }
  ]
}
```
