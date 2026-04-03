# solana-getTransactionCount

> getTransactionCount

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getTransactionCount`

## Parameters

Array of 0-1 item(s). . 1. Configuration Object ( )

## Returns

- **result** (`integer`): The current Transaction count from the ledger

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getTransactionCount",
  "params": [
    {
      "commitment": "finalized"
    }
  ]
}
```
