# sui-unsafe_moveCall

> Creates an unsigned transaction to execute a Move function call.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_moveCall

## Supported Chains
sui (mainnet)

## Method
`unsafe_moveCall`

## Parameters
Array of 8 items:

1. **signer** (`string`, required): The transaction signer's Sui address.

2. **package_object_id** (`string`, required): The Move package object ID containing the module.

3. **module** (`string`, required): The Move module name.

4. **function** (`string`, required): The Move function name to call.

5. **type_arguments** (`array` of `string`, optional): Array of type argument strings for generic functions (e.g., `["0x2::sui::SUI"]`). Default: `[]`.

6. **arguments** (`array`, required): Array of function arguments. Each argument can be:
   - A string for object IDs or pure values.
   - A number or boolean for primitive types.
   - An array for vector types.

7. **gas** (`string` | `null`, optional): The gas object ID to use for payment. If `null`, the system selects automatically.

8. **gas_budget** (`string`, required): The gas budget for the transaction in MIST.

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
  "method": "unsafe_moveCall",
  "params": [
    "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3",
    "0x2",
    "coin",
    "split",
    ["0x2::sui::SUI"],
    [
      "0xa1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0",
      "1000000000"
    ],
    null,
    "10000000"
  ]
}
```
