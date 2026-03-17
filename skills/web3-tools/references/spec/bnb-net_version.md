# bnb-net_version

> net_version

- **Category**: Node API - Bnb (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/bnb-net_version

## Supported Chains

Bnb (mainnet, testnet)

## Method

`net_version`

## Parameters

None - this method takes no parameters.

## Returns

- **result** (`string`): An integer encoded as a hexadecimal string (e.g., `'0x1a'`).

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "net_version"
}
```
