# kaia-kaia_newfilter

> kaia_newFilter

- **Category**: Node API - Kaia (JSON-RPC)

## Supported Chains

Kaia (mainnet, kairos)

## Method

`kaia_newFilter`

## Parameters

None - this method takes no parameters.

## Returns

- **result** (`string`): An integer encoded as a hexadecimal string (e.g., `'0x1a'`).

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "kaia_newFilter",
  "params": [
    {
      "fromBlock": "latest"
    }
  ]
}
```
