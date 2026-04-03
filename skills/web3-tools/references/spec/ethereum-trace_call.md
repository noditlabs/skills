# ethereum-trace_call

> trace_call

- **Category**: Node API - Ethereum (JSON-RPC)

## Supported Chains

Ethereum (mainnet, sepolia, hoodi)

## Method

`trace_call`

## Parameters

Array of parameters:

1. **Call Object** (`object` (optional)): The transaction call object.

   - `from` (string): transaction from address input.
   - `to` (string): transaction to address input.
   - `gas` (string): transaction hex input . contract call 0x0 input .
   - `gasPrice` (string): hex input.
   - `value` (string): transaction value value.
   - `data` (string): execution transaction method signature hashvalue . ABI .
2. **Trace Type** (`array` (optional)): Trace type chain transaction execution data . array value : - vmTrace: execution . status, status, execution result . - trace`: transaction execution . transaction . - `stateDiff`: transaction execution status . storage key value, balance code . transaction . chain transaction . - title: Block Number or Tag type: string pattern: ^0[xX][0-9a-fA-F]+$|^(latest|earliest|pending|safe|finalized)$ description: | . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `finalized`: finalized , status . (PoS) chain , finalized . - `safe`: network . ' ' network (reorgs) . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation . example: 'latest'

## Returns

An object containing:
- `gasUsed` (string): (hexadecimal)
- `output` (string): data (hexadecimal)

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "trace_call",
  "params": [
    {
      "from": "0xc90d3Ac75D1D36dF0b0a229E73D8409FB7F3c4ab",
      "to": "0xd3CdA913deB6f67967B99D67aCDFa1712C293601",
      "value": "0x186a0"
    },
    [
      "trace"
    ],
    "latest"
  ]
}
```
