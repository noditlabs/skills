# solana-getBlocksWithLimit

> getBlocksWithLimit

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getBlocksWithLimit`

## Parameters

Array of parameters:

1. **Start slot** (`any` (required)): 
2. **Limit** (`integer` (required)): Limit (must be no more than 500,000 blocks higher than the start_slot)
3. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.

## Returns

An array of objects. An array of u64 integers listing confirmed blocks starting at `start_slot` for up to `limit` blocks, inclusive.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlocksWithLimit",
  "params": [
    338967300,
    10
  ],
  "[object Object]": null
}
```
