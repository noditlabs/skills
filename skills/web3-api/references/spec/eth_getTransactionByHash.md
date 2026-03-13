# eth_getTransactionByHash

> Returns transaction information for a given transaction hash.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getTransactionByHash

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getTransactionByHash`

## Parameters
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `params` | `array` | Yes | Array of 1 item |
| `params[0]` - Transaction Hash | `string` | Yes | The transaction hash as a 64-character hex string (e.g., `"0xda148d856aef6d77..."`) |

## Returns
A transaction object, or `null` when no transaction was found. The transaction object contains:
- `blockHash` - Hash of the block containing the transaction
- `blockNumber` - Block number containing the transaction
- `from` - Address of the sender
- `gas` - Gas provided by the sender
- `gasPrice` - Gas price in wei
- `maxPriorityFeePerGas` - Max priority fee per gas (EIP-1559)
- `maxFeePerGas` - Max fee per gas (EIP-1559)
- `hash` - Transaction hash
- `input` - Data sent along with the transaction
- `nonce` - Number of transactions made by the sender prior to this one
- `to` - Address of the receiver
- `transactionIndex` - Transaction index position in the block
- `value` - Value transferred in wei
- `type` - Transaction type
- `accessList` - List of addresses and storage keys (EIP-2930)
- `chainId` - Chain ID
- `v`, `r`, `s` - ECDSA signature values

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByHash",
  "params": [
    "0xda148d856aef6d77d0b76c90ef1091ffe77afe9ee9b1c6cc23f28f042f198bd8"
  ]
}
```
