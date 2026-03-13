# polygon-bor_getSignersAtHash

> Returns the list of validators (signers) that signed a specific block identified by its hash, allowing identification of which nodes participated in block validation at a particular point in time.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/polygon-bor_getSignersAtHash

## Supported Chains
- Polygon

## Method
`bor_getSignersAtHash`

## Parameters
An array containing:

1. **Block Hash** (`string`, required): The block hash to query signers for. A 64-character hex string prefixed with `0x`.
   - Example: `"0xa70c0bff4de8a59f521920deb8b6f3a4885845f2f418409f5fc8daade7717505"`

## Returns
An array of signer addresses (`string[]`): The Ethereum addresses of the validators that signed the specified block.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "bor_getSignersAtHash",
  "params": [
    "0xa70c0bff4de8a59f521920deb8b6f3a4885845f2f418409f5fc8daade7717505"
  ]
}
```
