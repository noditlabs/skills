# solana-getSignatureStatuses

> getSignatureStatuses

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getSignatureStatuses`

## Parameters

Array of 1-2 item(s). . 1. Transaction signatures ( ) 2. Configuration Object ( )

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (array): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getSignatureStatuses",
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
