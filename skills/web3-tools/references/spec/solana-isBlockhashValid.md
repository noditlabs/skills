# solana-isBlockhashValid

> isBlockhashValid

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`isBlockhashValid`

## Parameters

Array of parameters:

1. **Blockhash** (`any` (required)): 
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `minContextSlot` (string): The minimum slot at which the request can be evaluated.

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (boolean): Whether the blockhash is still valid or not

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 45,
  "method": "isBlockhashValid",
  "params": [
    "J7rBdM6AecPDEZp8aPq5iPSNKVkU5Q76F3oAV4eW5wsW",
    {
      "commitment": "processed"
    }
  ]
}
```
