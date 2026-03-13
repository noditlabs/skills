# solana-getLeaderSchedule

> Returns the leader schedule for an epoch

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getLeaderSchedule

## Supported Chains
solana (mainnet, devnet)

## Method
`getLeaderSchedule`

## Parameters
- **Epoch** (integer, optional): Fetch the leader schedule for the epoch that corresponds to the provided slot. If unspecified, the leader schedule for the current epoch is fetched.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `identity` (string): Only return results for this validator identity (base-58 encoded).

## Returns
Returns null if requested epoch is not found, otherwise an object where keys are validator identities (as base-58 encoded strings) and values are arrays of leader slot indices relative to the first slot in the requested epoch.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getLeaderSchedule",
  "params": [null, {
    "commitment": "processed",
    "identity": "dv2eQHeP4RFrJZ6UeiZWoc3XTtmtZCUKxxCApCDcRNV"
  }]
}
```
