# polygon-bor_getauthor

> bor_getAuthor

- **Category**: Node API - Polygon Bor (JSON-RPC)

## Supported Chains

Polygon (mainnet, amoy)

## Method

`bor_getAuthor`

## Parameters

Array of parameters:

1. **Block Number or Tag** (`string` (optional)): . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `finalized`: finalized , status . (PoS) chain , finalized . - `safe`: network . ' ' network (reorgs) . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation .

## Returns

- **result** (`string`): hexadecimal string . 0x .

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
