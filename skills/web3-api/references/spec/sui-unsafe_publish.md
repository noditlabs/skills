# sui-unsafe_publish

> Creates an unsigned transaction to publish a Move package to the Sui network.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_publish

## Supported Chains
sui (mainnet)

## Method
`unsafe_publish`

## Parameters
Array of 4 items:

1. **sender** (`string`, required): The transaction sender's Sui address.

2. **compiled_modules** (`array` of `string`, required): Array of Base64-encoded compiled Move module bytecodes.

3. **dependencies** (`array` of `string`, required): Array of package object IDs that this package depends on (e.g., `["0x1", "0x2"]` for Move stdlib and Sui framework).

4. **gas** (`string` | `null`, optional): The gas object ID to use for payment. If `null`, the system selects automatically.

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
  "method": "unsafe_publish",
  "params": [
    "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3",
    [
      "oRzrCwYAAAAKAQAIAggMAxQuBEICBUQrB2+IAQj3ASgKnwIKDKkC6wEN..."
    ],
    [
      "0x1",
      "0x2"
    ],
    null,
    "100000000"
  ]
}
```
