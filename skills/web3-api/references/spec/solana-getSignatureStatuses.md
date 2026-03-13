# solana-getSignatureStatuses

> Returns the statuses of a list of signatures

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getSignatureStatuses

## Supported Chains
solana (mainnet, devnet)

## Method
`getSignatureStatuses`

## Parameters
- **Transaction signatures** (array of strings, required): An array of transaction signatures to confirm, as base-58 encoded strings.
- **Configuration Object** (object, optional):
  - `searchTransactionHistory` (boolean): If true, search the full transaction history (not just recent cache).

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (array): Array of status objects (or null), each with:
  - `slot` (integer): The slot the transaction was processed.
  - `confirmations` (integer or null): Number of blocks since confirmation, null if finalized.
  - `err` (object or null): Error if transaction failed.
  - `confirmationStatus` (string, enum: `processed`, `confirmed`, `finalized`): The transaction's cluster confirmation status.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getSignatureStatuses",
  "params": [
    ["5VERv8NMvzbJMEkV8xnrLkEaWRtSz9CosKDYjCJjBRnbJLgp8uirBgmQpjKhoR4tjF3ZpRzrFmBV6UjKdiSZkQUW"],
    { "searchTransactionHistory": true }
  ]
}
```
