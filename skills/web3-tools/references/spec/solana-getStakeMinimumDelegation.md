# solana-getStakeMinimumDelegation

> getStakeMinimumDelegation

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getStakeMinimumDelegation

## Supported Chains

Solana (mainnet, devnet)

## Method

`getStakeMinimumDelegation`

## Parameters

Array of 0-1 item(s). . 1. Configuration Object ( )

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (integer): The stake minimum delegation, in lamports

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getStakeMinimumDelegation",
  "params": [
    {
      "commitment": "finalized"
    }
  ]
}
```
