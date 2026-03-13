# solana-getTransaction

> Returns transaction details for a confirmed transaction

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getTransaction

## Supported Chains
solana (mainnet, devnet)

## Method
`getTransaction`

## Parameters
- **Transaction signature** (string, required): Transaction signature, as base-58 encoded string.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `maxSupportedTransactionVersion` (integer, default: 0): Set to 0 to fetch all transactions.
  - `transactionDetails` (string, enum: `full`, `accounts`, `signatures`, `none`, default: `full`): Level of transaction detail.

## Returns
An object containing:
- `blockTime` (integer or null): Estimated production time as Unix timestamp.
- `meta` (object): Transaction metadata including `err`, `fee`, `preBalances`, `postBalances`, `innerInstructions`, `logMessages`, `rewards`, `loadedAddresses`, `computeUnitsConsumed`.
- `slot` (integer): The slot this transaction was processed in.
- `transaction` (object): Transaction data with `message` and `signatures`.
- `version` (string or number): Transaction version.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getTransaction",
  "params": [
    "5Pj5fCupXLUePYn18JkY8SrRaWFiUctuDTRwvUy2ML9yvkENLb1QMYbcBGcBXRrSVDjp7RjUwk9a3rLC6gpvtYpZ",
    { "commitment": "confirmed", "maxSupportedTransactionVersion": 0, "encoding": "json" }
  ]
}
```
