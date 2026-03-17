# optimism-eth_newfilter

> eth_newFilter

- **Category**: Node API - Optimism (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/optimism-eth_newfilter

## Supported Chains

Optimism (mainnet, sepolia)

## Method

`eth_newFilter`

## Parameters

None - this method takes no parameters.

## Returns

- **result** (`string`): An integer encoded as a hexadecimal string (e.g., `'0x1a'`).

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_newFilter",
  "params": [
    {
      "fromBlock": "latest"
    }
  ]
}
```
