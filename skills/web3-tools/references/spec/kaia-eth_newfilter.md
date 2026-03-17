# kaia-eth_newfilter

> eth_newFilter

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-eth_newfilter

## Supported Chains

Kaia (mainnet, kairos)

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
