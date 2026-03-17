# solana-getTokenSupply

> getTokenSupply

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getTokenSupply

## Supported Chains

Solana (mainnet, devnet)

## Method

`getTokenSupply`

## Parameters

Array of parameters:

1. **Pubkey of the token Mint** (`string` (required)): Pubkey of the token Mint to query, as base-58 encoded string
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
  "method": "getTokenSupply",
  "params": [
    "3wyAj7Rt1TWVPZVteFJPLa26JmLvdb1CAKEFZm3NY75E",
    {
      "commitment": "finalized"
    }
  ]
}
```
