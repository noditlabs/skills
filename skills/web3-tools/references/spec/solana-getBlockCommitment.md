# solana-getBlockCommitment

> getBlockCommitment

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getBlockCommitment`

## Parameters

Array of 1-1 item(s). Block number, identified by Slot.

## Returns

An object containing:
- `commitment` (array): Array of u64 integers logging the amount of cluster stake in lamports that has voted on the block at each depth from 0 to `MAX_LOCKOUT_HISTORY`.
- `totalStake` (integer): Total active stake, in lamports, of the current epoch.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlockCommitment",
  "params": [
    5
  ]
}
```
