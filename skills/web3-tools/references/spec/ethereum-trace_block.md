# ethereum-trace_block

> trace_block

- **Category**: Node API - Ethereum (JSON-RPC)

## Supported Chains

Ethereum (mainnet, sepolia, hoodi)

## Method

`trace_block`

## Parameters

Array of parameters:

1. **Block Number or Tag** (`string` (optional)): . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `finalized`: finalized , status . (PoS) chain , finalized . - `safe`: network . ' ' network (reorgs) . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation .

## Returns

An array of objects. execution object . trace_* .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "trace_block",
  "params": [
    "latest"
  ]
}
```
