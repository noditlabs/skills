# base-net_version

> net_version

- **Category**: Node API - Base (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/base-net_version

## Supported Chains

Base (mainnet, sepolia)

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
