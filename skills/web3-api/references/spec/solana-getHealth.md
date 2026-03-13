# solana-getHealth

> Returns the current health of the node

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getHealth

## Supported Chains
solana (mainnet, devnet)

## Method
`getHealth`

## Parameters
None.

## Returns
Either:
- `"ok"` if the node is healthy.
- A JSON RPC error response if the node is unhealthy (with optional `numSlotsBehind` data).

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getHealth"
}
```
