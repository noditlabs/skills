# solana-getSlotLeader

> getSlotLeader

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getSlotLeader

## Supported Chains

Solana (mainnet, devnet)

## Method

`getSlotLeader`

## Parameters

Array of 0-1 item(s). . 1. Configuration Object ( )

## Returns

- **result** (`string`): Node identity Pubkey as base-58 encoded string

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getSlotLeader",
  "params": [
    {
      "commitment": "finalized"
    }
  ]
}
```
