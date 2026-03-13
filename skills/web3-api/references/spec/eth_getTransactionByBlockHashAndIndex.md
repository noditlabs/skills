# eth_getTransactionByBlockHashAndIndex

> Returns transaction information by block hash and transaction index position.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getTransactionByBlockHashAndIndex

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getTransactionByBlockHashAndIndex`

## Parameters
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `params` | `array` | Yes | Array of 2 items |
| `params[0]` - Block Hash | `string` | Yes | The block hash as a 64-character hex string (e.g., `"0x59f63e3840..."`) |
| `params[1]` - Transaction Index | `string` | Yes | The transaction index position in the block as a hex string (e.g., `"0x0"`) |

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
  "method": "eth_getTransactionByBlockHashAndIndex",
  "params": [
    "0x59f63e3840e0f4a1659074c1a4021e881a268a52d31958688da1d66bfbf6d2ca",
    "0x0"
  ]
}
```
