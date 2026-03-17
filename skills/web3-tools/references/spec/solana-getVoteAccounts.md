# solana-getVoteAccounts

> getVoteAccounts

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getVoteAccounts

## Supported Chains

Solana (mainnet, devnet)

## Method

`getVoteAccounts`

## Parameters

Array of 0-1 item(s). . 1. Configuration Object ( )

## Returns

An object containing:
- `current` (array): validator vote array.
- `delinquent` (array): vote array.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getVoteAccounts",
  "params": [
    {
      "commitment": "finalized",
      "votePubkey": "i7NyKBMJCA9bLM2nsGyAGCKHECuR2L5eh4GqFciuwNT"
    }
  ]
}
```
