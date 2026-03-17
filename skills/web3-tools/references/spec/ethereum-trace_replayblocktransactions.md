# ethereum-trace_replayblocktransactions

> trace_replayBlockTransactions

- **Category**: Node API - Ethereum (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/ethereum-trace_replayblocktransactions

## Supported Chains

Ethereum (mainnet, sepolia, hoodi)

## Method

`trace_replayBlockTransactions`

## Parameters

Array of parameters:

1. **Block Number or Tag** (`string` (optional)): . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `finalized`: finalized , status . (PoS) chain , finalized . - `safe`: network . ' ' network (reorgs) . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation .
2. **Trace Type** (`array` (optional)): Trace type chain transaction execution data . array value : - vmTrace: execution . status, status, execution result . - trace`: transaction execution . transaction . - `stateDiff`: transaction execution status . storage key value, balance code . transaction . chain transaction .

## Returns

An array of objects. execution object . trace_* .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "trace_replayBlockTransactions",
  "params": [
    "latest",
    [
      "trace"
    ]
  ]
}
```
