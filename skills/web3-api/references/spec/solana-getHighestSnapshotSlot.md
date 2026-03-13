# solana-getHighestSnapshotSlot

> Returns the highest slot information that the node has snapshots for

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getHighestSnapshotSlot

## Supported Chains
solana (mainnet, devnet)

## Method
`getHighestSnapshotSlot`

## Parameters
None.

## Returns
An object containing:
- `full` (integer): The highest full snapshot slot (uint64).
- `incremental` (integer): The highest incremental snapshot slot based on full (uint64).

Or an error object if no snapshot is available.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getHighestSnapshotSlot"
}
```
