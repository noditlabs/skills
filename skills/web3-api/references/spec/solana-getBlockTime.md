# solana-getBlockTime

> Returns the estimated production time of a block

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBlockTime

## Supported Chains
solana (mainnet, devnet)

## Method
`getBlockTime`

## Parameters
- **Block number** (integer, required): Block number, identified by Slot (uint64).

## Returns
Either:
- An integer: Estimated production time, as Unix timestamp (seconds since the Unix epoch).
- An error object if the block time is unavailable.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlockTime",
  "params": [338967300]
}
```
