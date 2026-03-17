# bnb-eth_getlogs

> eth_getLogs

- **Category**: Node API - Bnb (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/bnb-eth_getlogs

## Supported Chains

Bnb (mainnet, testnet)

## Method

`eth_getLogs`

## Parameters

None - this method takes no parameters.

## Returns

An array of objects. event object . transaction execution event .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getLogs",
  "params": [
    {
      "fromBlock": "latest"
    }
  ]
}
```
