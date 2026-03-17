# solana-getRecentPrioritizationFees

> getRecentPrioritizationFees

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getRecentPrioritizationFees

## Supported Chains

Solana (mainnet, devnet)

## Method

`getRecentPrioritizationFees`

## Parameters

Array of 0-1 item(s). An array of Account addresses (up to a maximum of 128 addresses), as base-58 encoded strings. If this parameter is provided, the response will reflect a fee to land a transaction locking all of the provided accounts as writable.

## Returns

An array of objects. 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getRecentPrioritizationFees",
  "params": [
    [
      "CxELquR1gPP8wHe33gZ4QxqGB3sZ9RSwsJ2KshVewkFY"
    ]
  ]
}
```
