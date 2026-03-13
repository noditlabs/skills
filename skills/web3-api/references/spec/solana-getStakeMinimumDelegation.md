# solana-getStakeMinimumDelegation

> Returns the stake minimum delegation, in lamports

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getStakeMinimumDelegation

## Supported Chains
solana (mainnet, devnet)

## Method
`getStakeMinimumDelegation`

## Parameters
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (integer): The stake minimum delegation, in lamports (uint64).

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getStakeMinimumDelegation",
  "params": [{ "commitment": "finalized" }]
}
```
