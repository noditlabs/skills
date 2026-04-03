# luniverse-eth_estimategas

> eth_estimateGas

- **Category**: Node API - Luniverse (JSON-RPC)

## Supported Chains

Luniverse (mainnet)

## Method

`eth_estimateGas`

## Parameters

Array of parameters:

1. **Call Object** (`object` (optional)): The transaction call object.

   - `from` (string): transaction from address input.
   - `to` (string): transaction to address input.
   - `gas` (string): transaction hex input . contract call 0x0 input .
   - `gasPrice` (string): hex input.
   - `value` (string): transaction value value.
   - `data` (string): execution transaction method signature hashvalue . ABI .

## Returns

- **result** (`string`): An integer encoded as a hexadecimal string (e.g., `'0x1a'`).

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_estimateGas",
  "params": [
    {
      "from": "0xc90d3Ac75D1D36dF0b0a229E73D8409FB7F3c4ab",
      "to": "0xd3CdA913deB6f67967B99D67aCDFa1712C293601",
      "value": "0x186a0"
    }
  ]
}
```
