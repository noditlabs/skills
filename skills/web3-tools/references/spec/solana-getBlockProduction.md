# solana-getBlockProduction

> getBlockProduction

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBlockProduction

## Supported Chains

Solana (mainnet, devnet)

## Method

`getBlockProduction`

## Parameters

Array of 0-1 item(s). . 1. Configuration Object ( )

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (integer): The lamport balance of the account

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlockProduction",
  "params": [
    {
      "commitment": "finalized",
      "identity": "12i8gndWWWMTRzJBFhnYkobNgZB3XMUUJq75HeUrshrk",
      "range": {
        "firstSlot": 363067597,
        "lastSlot": 364115359
      }
    }
  ]
}
```
