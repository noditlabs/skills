# base-eth_chainid

> eth_chainId

- **Category**: Node API - Base (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/base-eth_chainid

## Supported Chains

Base (mainnet, sepolia)

## Method

`eth_chainId`

## Parameters

None - this method takes no parameters.

## Returns

- **result** (`string`): An integer encoded as a hexadecimal string (e.g., `'0x1a'`).

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_chainId"
}
```
