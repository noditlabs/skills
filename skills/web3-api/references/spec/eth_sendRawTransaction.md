# eth_sendRawTransaction

> Submits a pre-signed transaction to the network. Returns the transaction hash on success.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_sendRawTransaction

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_sendRawTransaction`

## Parameters
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `params` | `array` | Yes | Array of 1 item |
| `params[0]` - Signed Transaction Data | `string` | Yes | The signed transaction data as a hex string. The transaction must be signed client-side with a private key. The node only validates the transaction. To produce signed transaction data: 1) Create transaction data (from, to, gas, value, etc.) 2) RLP-encode the data 3) Hash with Keccak-256 4) Sign with private key |

## Returns
The transaction hash as a hex string if the transaction was successfully submitted to the network (e.g., `"0x0100000000000000ee32c7a8d24aac1f"`).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_sendRawTransaction",
  "params": [
    "0x02f8688080808080943f39cfbaff46cb736a603269d14a7e9adf5158b488016345785d8a000080c001a005599173ee4483fa38044e8d7bf592b58a9ab598f7d4a510702d193c60af15a0a00f2d39e8202dc9d7d66a51fc67fcf1d893b20e080c6acf2b25610f5e926cfa21"
  ]
}
```
