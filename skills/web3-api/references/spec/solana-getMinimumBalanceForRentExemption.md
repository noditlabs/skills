# solana-getMinimumBalanceForRentExemption

> Returns minimum balance required to make account rent exempt

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getMinimumBalanceForRentExemption

## Supported Chains
solana (mainnet, devnet)

## Method
`getMinimumBalanceForRentExemption`

## Parameters
- **Account's Data Length** (integer, required): The length of the account's data.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.

## Returns
An integer (uint64): Minimum lamports required in the Account to remain rent free.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getMinimumBalanceForRentExemption",
  "params": [50, { "commitment": "processed" }]
}
```
