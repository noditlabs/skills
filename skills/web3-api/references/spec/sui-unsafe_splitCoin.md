# sui-unsafe_splitCoin

> Creates an unsigned transaction to split a coin into multiple coins with specified amounts.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_splitCoin

## Supported Chains
sui (mainnet)

## Method
`unsafe_splitCoin`

## Parameters
Array of 5 items:

1. **signer** (`string`, required): The transaction signer's Sui address.

2. **coin_object_id** (`string`, required): The object ID of the coin to split.

3. **split_amounts** (`array` of `string`, required): Array of amounts (in MIST) for each new coin to create from the split.

4. **gas** (`string` | `null`, optional): The gas object ID to use for payment. If `null`, the system selects automatically. Must not be the same as `coin_object_id`.

5. **gas_budget** (`string`, required): The gas budget for the transaction in MIST.

## Returns
- **TransactionBytes** (`object`): The unsigned transaction bytes.
  - `txBytes` (`string`): Base64-encoded BCS serialized transaction data.
  - `gas` (`array`): Array of gas object references used.
  - `inputObjects` (`array`): Array of input object metadata.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "unsafe_splitCoin",
  "params": [
    "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3",
    "0xa1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0",
    [
      "1000000000",
      "2000000000"
    ],
    null,
    "10000000"
  ]
}
```
