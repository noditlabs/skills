# polygon-bor_getAuthor

> Returns the address of the validator (block author/miner) that produced a specific block on the Polygon PoA network.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/polygon-bor_getAuthor

## Supported Chains
- Polygon

## Method
`bor_getAuthor`

## Parameters
An array containing:

1. **Block Number or Tag** (`string`, required): The block to query.
   - Block number as hex string (e.g., `"0x12C1A00"`)
   - Block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`

## Returns
- `result` (`string`): The address of the block author/validator.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "bor_getAuthor",
  "params": [
    "latest"
  ]
}
```
