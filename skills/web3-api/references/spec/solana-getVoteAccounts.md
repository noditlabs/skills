# solana-getVoteAccounts

> Returns the account info and associated stake for all the voting accounts in the current bank

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getVoteAccounts

## Supported Chains
solana (mainnet, devnet)

## Method
`getVoteAccounts`

## Parameters
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `votePubkey` (string): Only return results for this validator vote address (base-58 encoded).
  - `keepUnstakedDelinquents` (boolean): Do not filter out delinquent validators with no stake.
  - `delinquentSlotDistance` (integer): Specify the number of slots behind the tip that a validator must fall to be considered delinquent.

## Returns
An object containing:
- `current` (array): Array of all vote accounts currently participating in the validator set, each with `activatedStake`, `commission`, `epochCredits`, `epochVoteAccount`, `lastVote`, `nodePubkey`, `rootSlot`, `votePubkey`.
- `delinquent` (array): Array of all delinquent vote accounts with same fields.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getVoteAccounts",
  "params": [{
    "commitment": "finalized",
    "votePubkey": "i7NyKBMJCA9bLM2nsGyAGCKHECuR2L5eh4GqFciuwNT"
  }]
}
```
