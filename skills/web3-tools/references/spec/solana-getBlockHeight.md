# solana-getBlockHeight

> getBlockHeight

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getBlockHeight`

## Parameters

Array of 0-1 item(s). . 1. Configuration Object ( )

## Returns

- **result** (`integer`): Current block height.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlockHeight",
  "params": [
    {
      "commitment": "finalized",
      "minContextSlot": "342288570"
    }
  ]
}
```
