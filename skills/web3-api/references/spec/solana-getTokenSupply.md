# solana-getTokenSupply

> Returns the total supply of an SPL Token type

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getTokenSupply

## Supported Chains
solana (mainnet, devnet)

## Method
`getTokenSupply`

## Parameters
- **Pubkey of the token Mint** (string, required): Pubkey of the token Mint to query, as base-58 encoded string.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (object):
  - `amount` (string): The raw amount without decimals, a string representation of u64.
  - `decimals` (number): Number of base 10 digits to the right of the decimal place.
  - `uiAmount` (number): The total token supply, using mint-prescribed decimals.
  - `uiAmountString` (string): The total token supply as a string.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getTokenSupply",
  "params": ["3wyAj7Rt1TWVPZVteFJPLa26JmLvdb1CAKEFZm3NY75E", { "commitment": "finalized" }]
}
```
