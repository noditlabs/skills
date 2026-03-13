# solana-getTransactionCount

> Returns the current Transaction count from the ledger

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getTransactionCount

## Supported Chains
solana (mainnet, devnet)

## Method
`getTransactionCount`

## Parameters
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.

## Returns
An integer: The current Transaction count from the ledger.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getTransactionCount",
  "params": [{ "commitment": "finalized" }]
}
```
