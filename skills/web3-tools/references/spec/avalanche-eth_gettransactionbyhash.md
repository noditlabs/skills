# avalanche-eth_gettransactionbyhash

> eth_getTransactionByHash

- **Category**: Node API - Avalanche (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/avalanche-eth_gettransactionbyhash

## Supported Chains

Avalanche (mainnet, fuji)

## Method

`eth_getTransactionByHash`

## Parameters

Array of parameters:

1. **Transaction Hash** (`string` (optional)): The transaction hash as a 64-character hexadecimal string.

## Returns

An object containing:
- `blockHash` (string): transaction block hash. confirmation transaction null
- `blockNumber` (string): transaction block number (hexadecimal). confirmation null
- `from` (string): transaction sender address
- `gas` (string): transaction gas limit (hexadecimal)
- `gasPrice` (string): (hexadecimal, wei )
- `maxPriorityFeePerGas` (string): fee (EIP-1559, hexadecimal)
- `maxFeePerGas` (string): fee (EIP-1559, hexadecimal)
- `hash` (string): transaction hash
- `input` (string): transaction input data (hexadecimal)
- `nonce` (string): sender transaction count (hexadecimal)

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
