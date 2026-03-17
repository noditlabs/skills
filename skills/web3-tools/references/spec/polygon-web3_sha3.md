# polygon-web3_sha3

> web3_sha3

- **Category**: Node API - Polygon (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/polygon-web3_sha3

## Supported Chains

Polygon (mainnet, amoy)

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
