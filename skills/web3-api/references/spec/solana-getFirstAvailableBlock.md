# solana-getFirstAvailableBlock

> Returns the slot of the lowest confirmed block that has not been purged from the ledger

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getFirstAvailableBlock

## Supported Chains
solana (mainnet, devnet)

## Method
`getFirstAvailableBlock`

## Parameters
None.

## Returns
An integer representing the slot of the lowest confirmed block that has not been purged from the ledger.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getFirstAvailableBlock"
}
```
