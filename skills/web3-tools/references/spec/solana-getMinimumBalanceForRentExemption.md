# solana-getMinimumBalanceForRentExemption

> getMinimumBalanceForRentExemption

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getMinimumBalanceForRentExemption`

## Parameters

Array of parameters:

1. **Account's Data Length** (`integer` (required)): The length of the account's data
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.

## Returns

- **result** (`integer`): Minimum lamports required in the Account to remain rent free

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getMinimumBalanceForRentExemption",
  "params": [
    50,
    {
      "commitment": "processed"
    }
  ]
}
```
