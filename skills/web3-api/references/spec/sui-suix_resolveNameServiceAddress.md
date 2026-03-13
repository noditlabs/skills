# sui-suix_resolveNameServiceAddress

> Resolves a SuiNS (Sui Name Service) name to its associated Sui address.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_resolveNameServiceAddress

## Supported Chains
sui (mainnet)

## Method
`suix_resolveNameServiceAddress`

## Parameters
Array of 1 item:

1. **name** (`string`, required): The SuiNS name to resolve (e.g., `"example.sui"`).

## Returns
- **result** (`string` | `null`): The Sui address associated with the given name, or `null` if the name is not registered.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_resolveNameServiceAddress",
  "params": [
    "example.sui"
  ]
}
```
