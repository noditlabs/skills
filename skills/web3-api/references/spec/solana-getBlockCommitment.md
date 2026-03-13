# solana-getBlockCommitment

> Returns commitment for a particular block

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBlockCommitment

## Supported Chains
solana (mainnet, devnet)

## Method
`getBlockCommitment`

## Parameters
- **Block number** (integer, required): Block number, identified by Slot (uint64).

## Returns
An object containing:
- `commitment` (array of integers): Array of u64 integers logging the amount of cluster stake in lamports that has voted on the block at each depth from 0 to MAX_LOCKOUT_HISTORY.
- `totalStake` (integer): Total active stake, in lamports, of the current epoch.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlockCommitment",
  "params": [5]
}
```
