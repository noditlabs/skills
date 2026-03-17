# ethereum-trace_replaytransaction

> trace_replayTransaction

- **Category**: Node API - Ethereum (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/ethereum-trace_replaytransaction

## Supported Chains

Ethereum (mainnet, sepolia, hoodi)

## Method

`trace_replayTransaction`

## Parameters

Array of parameters:

1. **Transaction Hash** (`string` (optional)): The transaction hash as a 64-character hexadecimal string.
2. **Trace Type** (`array` (optional)): Trace type chain transaction execution data . array value : - vmTrace: execution . status, status, execution result . - trace`: transaction execution . transaction . - `stateDiff`: transaction execution status . storage key value, balance code . transaction . chain transaction .

## Returns

An object containing:
- `gasUsed` (string): (hexadecimal)
- `output` (string): data (hexadecimal)

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "trace_replayTransaction",
  "params": [
    "0x17104ac9d3312d8c136b7f44d4b8b47852618065ebfa534bd2d3b5ef218ca1f3",
    [
      "trace"
    ]
  ]
}
```
