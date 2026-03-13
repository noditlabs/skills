# solana-isBlockhashValid

> Returns whether a blockhash is still valid or not

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-isBlockhashValid

## Supported Chains
solana (mainnet, devnet)

## Method
`isBlockhashValid`

## Parameters
- **Blockhash** (string, required): The blockhash of the block, as base-58 encoded string.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (boolean): Whether the blockhash is still valid or not.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 45,
  "method": "isBlockhashValid",
  "params": ["J7rBdM6AecPDEZp8aPq5iPSNKVkU5Q76F3oAV4eW5wsW", { "commitment": "processed" }]
}
```
