# solana-getSignaturesForAddress

> Returns signatures for confirmed transactions that include the given address in their accountKeys list

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getSignaturesForAddress

## Supported Chains
solana (mainnet, devnet)

## Method
`getSignaturesForAddress`

## Parameters
- **Account address** (string, required): Account address, as base-58 encoded string.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `limit` (integer): Maximum transaction signatures to return (1-1000, default: 1000).
  - `before` (string): Start searching backwards from this transaction signature.
  - `until` (string): Search until this transaction signature.

## Returns
An array of objects, each containing:
- `signature` (string): Transaction signature as base-58 encoded string.
- `slot` (integer): The slot that contains the block with the transaction.
- `err` (object or null): Error if transaction failed.
- `memo` (string or null): Memo associated with the transaction.
- `blockTime` (integer or null): Estimated production time as Unix timestamp.
- `confirmationStatus` (string): The transaction's cluster confirmation status.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getSignaturesForAddress",
  "params": [
    "Vote111111111111111111111111111111111111111",
    { "commitment": "finalized", "limit": 1 }
  ]
}
```
