# arc-eth_getunclecountbyblocknumber

> eth_getUncleCountByBlockNumber

- **Category**: Node API - Arc (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/arc-eth_getunclecountbyblocknumber

## Supported Chains

Arc (testnet)

## Method

`eth_getUncleCountByBlockNumber`

## Parameters

Array of parameters:

1. **Block Number or Tag** (`string` (optional)): . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `finalized`: finalized , status . (PoS) chain , finalized . - `safe`: network . ' ' network (reorgs) . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation .

## Returns

- **result** (`string`): An integer encoded as a hexadecimal string (e.g., `'0x1a'`).

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getUncleCountByBlockNumber",
  "params": [
    "0x5BAD54"
  ]
}
```
