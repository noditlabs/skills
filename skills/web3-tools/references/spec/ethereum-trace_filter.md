# ethereum-trace_filter

> trace_filter

- **Category**: Node API - Ethereum (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/ethereum-trace_filter

## Supported Chains

Ethereum (mainnet, sepolia, hoodi)

## Method

`trace_filter`

## Parameters

Array of parameters:

1. **Trace Object** (`object` (optional)): Trace filter Object input.

   - `fromBlock` (string): . hexadecimal string .
   - `toBlock` (string): . hexadecimal string .
   - `fromAddress` (array): filter from address array input.
   - `toAddress` (array): filter to address array input.
   - `after` (string): trace offset size.
   - `count` (integer): trace batch trace .

## Returns

An array of objects. execution object . trace_* .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "trace_filter",
  "params": [
    {
      "fromBlock": "0x1253B3F",
      "toBlock": "0x1253B5F",
      "fromAddress": [
        "0xB287eaC48aB21c5FB1d3723830d60b4c797555B0"
      ]
    }
  ]
}
```
