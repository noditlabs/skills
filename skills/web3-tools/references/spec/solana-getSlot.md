# solana-getSlot

> getSlot

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getSlot`

## Parameters

Array of 0-1 item(s). . 1. Configuration Object ( )

## Returns

- **result** (`integer`): slot

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getSlot",
  "params": [
    [
      "5VERv8NMvzbJMEkV8xnrLkEaWRtSz9CosKDYjCJjBRnbJLgp8uirBgmQpjKhoR4tjF3ZpRzrFmBV6UjKdiSZkQUW"
    ],
    {
      "searchTransactionHistory": true
    }
  ]
}
```
