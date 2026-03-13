# solana-getTokenAccountBalance

> Returns the token balance of an SPL Token account

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getTokenAccountBalance

## Supported Chains
solana (mainnet, devnet)

## Method
`getTokenAccountBalance`

## Parameters
- **Pubkey of Token Account** (string, required): Pubkey of Token account to query, as base-58 encoded string.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (object):
  - `amount` (string): The raw balance without decimals, a string representation of u64.
  - `decimals` (number): Number of base 10 digits to the right of the decimal place.
  - `uiAmount` (number): DEPRECATED. The balance, using mint-prescribed decimals.
  - `uiAmountString` (string): The balance as a string, using mint-prescribed decimals.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getTokenAccountBalance",
  "params": ["7fUAJdStEuGbc3sM84cKRL6yYaaSstyLSU4ve5oovLS7", { "commitment": "finalized" }]
}
```
