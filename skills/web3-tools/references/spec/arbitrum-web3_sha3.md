# arbitrum-web3_sha3

> web3_sha3

- **Category**: Node API - Arbitrum (JSON-RPC)

## Supported Chains

Arbitrum (mainnet, sepolia)

## Method

`web3_sha3`

## Parameters

Array of parameters:

1. **입력 데이터** (`string` (optional)): SHA3 hash data . value hexadecimal encoding , '0x' . , "0x68656c6c6f204e4f444954" "hello NODIT".

## Returns

- **result** (`string`): hexadecimal string . 0x .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "web3_sha3",
  "params": [
    "0x68656c6c6f204e4f444954"
  ]
}
```
