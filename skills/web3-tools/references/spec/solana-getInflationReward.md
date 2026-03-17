# solana-getInflationReward

> getInflationReward

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getInflationReward

## Supported Chains

Solana (mainnet, devnet)

## Method

`getInflationReward`

## Parameters

Array of parameters:

1. **Addresses** (`array` (optional)): An array of addresses to query, as base-58 encoded strings
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `epoch` (string): The blockhash of query, as base-58 encoded string
   - `minContextSlot` (string): The minimum slot at which the request can be evaluated.

## Returns

An object containing:
- `epoch` (integer): Epoch for which reward occurred
- `effectiveSlot` (integer): The slot in which the rewards are effective
- `amount` (integer): Reward amount in lamports
- `postBalance` (integer): Post balance of the account in lamports
- `commission` (integer): Vote account commission when the reward was credited

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getInflationReward",
  "params": [
    [
      "6dmNQ5jwLeLk5REvio1JcMshcbvkYMwy26sJ8pbkvStu",
      "BGsqMegLpV6n6Ve146sSX2dTjUMj3M92HnU8BbNRMhF2"
    ],
    {
      "epoch": 800,
      "commitment": "finalized"
    }
  ]
}
```
