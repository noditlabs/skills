# ethereum-eth_gettransactionreceipt

> eth_getTransactionReceipt

- **Category**: Node API - Ethereum (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/ethereum-eth_gettransactionreceipt

## Supported Chains

Ethereum (mainnet, sepolia, hoodi)

## Method

`eth_getTransactionReceipt`

## Parameters

Array of parameters:

1. **Transaction Hash** (`string` (optional)): The transaction hash as a 64-character hexadecimal string.

## Returns

An object containing:
- `blockHash` (string): transaction block hash
- `blockNumber` (string): transaction block number (hexadecimal)
- `contractAddress` (string): contract creation transaction creation contract address, null
- `cumulativeGasUsed` (string): transaction (hexadecimal)
- `effectiveGasPrice` (string): (hexadecimal, wei )
- `from` (string): transaction sender address
- `gasUsed` (string): transaction (hexadecimal)
- `logs` (array): transaction execution event
- `logsBloom` (string): event Bloom filter (2048 , hexadecimal)
- `status` (string): transaction execution result (0x1= , 0x0= )

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionReceipt",
  "params": [
    "0xda148d856aef6d77d0b76c90ef1091ffe77afe9ee9b1c6cc23f28f042f198bd8"
  ]
}
```
