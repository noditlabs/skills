# solana-getBlocks

> getBlocks

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBlocks

## Supported Chains

Solana (mainnet, devnet)

## Method

`getBlocks`

## Parameters

Array of parameters:

1. **Start slot** (`any` (required)): 
2. **End slot** (`any` (optional)): 
3. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.

## Returns

An array of objects. An array of u64 integers listing confirmed blocks between `start_slot` and either `end_slot` - if provided, or latest confirmed slot, inclusive. Max range allowed is 500,000 slots.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlocks",
  "params": [
    338967300,
    338967310,
    {
      "commitment": "finalized"
    }
  ]
}
```
