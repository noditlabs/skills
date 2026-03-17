# ethereum-eth_chainid

> eth_chainId

- **Category**: Node API - Ethereum (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/ethereum-eth_chainid

## Supported Chains

Ethereum (mainnet, sepolia, hoodi)

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
