# kaia-kaia_getlogs

> kaia_getLogs

- **Category**: Node API - Kaia (JSON-RPC)

## Supported Chains

Kaia (mainnet, kairos)

## Method

`kaia_getLogs`

## Parameters

None - this method takes no parameters.

## Returns

An array of objects. event object . transaction execution event .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "kaia_getLogs",
  "params": [
    {
      "fromBlock": "latest"
    }
  ]
}
```
