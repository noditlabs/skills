# solana-getSupply

> Returns information about the current supply

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getSupply

## Supported Chains
solana (mainnet, devnet)

## Method
`getSupply`

## Parameters
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `excludeNonCirculatingAccountsList` (boolean): Exclude non circulating accounts list from response.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (object):
  - `total` (integer): Total supply in lamports.
  - `circulating` (integer): Circulating supply in lamports.
  - `nonCirculating` (integer): Non-circulating supply in lamports.
  - `nonCirculatingAccounts` (array of strings): Array of account addresses of non-circulating accounts.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getSupply",
  "params": [{ "commitment": "finalized", "excludeNonCirculatingAccountsList": true }]
}
```
