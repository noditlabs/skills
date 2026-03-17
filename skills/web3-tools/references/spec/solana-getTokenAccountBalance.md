# solana-getTokenAccountBalance

> getTokenAccountBalance

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getTokenAccountBalance

## Supported Chains

Solana (mainnet, devnet)

## Method

`getTokenAccountBalance`

## Parameters

Array of parameters:

1. **Pubkey of Token Account** (`string` (required)): Pubkey of Token account to query, as base-58 encoded string
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (object): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getTokenAccountBalance",
  "params": [
    "7fUAJdStEuGbc3sM84cKRL6yYaaSstyLSU4ve5oovLS7",
    {
      "commitment": "finalized"
    }
  ]
}
```
