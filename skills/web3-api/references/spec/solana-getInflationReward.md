# solana-getInflationReward

> Returns the inflation/staking reward for a list of addresses for an epoch

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getInflationReward

## Supported Chains
solana (mainnet, devnet)

## Method
`getInflationReward`

## Parameters
- **Addresses** (array of strings, optional): An array of addresses to query, as base-58 encoded strings.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `epoch` (string): The epoch to query rewards for.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.

## Returns
An array of objects (or null for addresses with no reward), each containing:
- `epoch` (integer): Epoch for which reward occurred.
- `effectiveSlot` (integer): The slot in which the rewards are effective.
- `amount` (integer): Reward amount in lamports.
- `postBalance` (integer): Post balance of the account in lamports.
- `commission` (integer): Vote account commission when the reward was credited.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getInflationReward",
  "params": [
    ["6dmNQ5jwLeLk5REvio1JcMshcbvkYMwy26sJ8pbkvStu"],
    { "epoch": 800, "commitment": "finalized" }
  ]
}
```
