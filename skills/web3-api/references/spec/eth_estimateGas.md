# eth_estimateGas

> Estimates the gas required to execute a transaction without actually sending it.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_estimateGas

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_estimateGas`

## Parameters
Array of exactly 1 item:

1. **Call Object** (`object`): The transaction call object.
   - `from` (`string`, optional): The sender address.
   - `to` (`string`, required): The recipient/contract address.
   - `gas` (`string`, optional): Gas limit in hex.
   - `gasPrice` (`string`, optional): Gas price in hex.
   - `value` (`string`, optional): Value to send in hex.
   - `data` (`string`, optional): The encoded method signature and parameters (ABI-encoded).

## Returns
- **result** (`string`): The estimated gas amount as a hexadecimal string (e.g., `"0x5208"` for a simple transfer = 21000 gas).

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
