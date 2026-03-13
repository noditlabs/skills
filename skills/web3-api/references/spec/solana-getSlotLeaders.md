# solana-getSlotLeaders

> Returns the slot leaders for a given slot range

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getSlotLeaders

## Supported Chains
solana (mainnet, devnet)

## Method
`getSlotLeaders`

## Parameters
- **StartSlot** (integer, required): The slot number (uint64).
- **Limit** (integer, required): The limit of the result. Must be between 1 and 500,000 (uint64).

## Returns
An array of Node identity public keys as base-58 encoded strings.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getSlotLeaders",
  "params": [100, 10]
}
```
