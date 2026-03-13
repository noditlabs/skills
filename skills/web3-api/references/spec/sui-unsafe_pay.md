# sui-unsafe_pay

> Creates an unsigned transaction to send coins of any type to a list of recipients. Unlike unsafe_paySui, the input coins and gas coin are separate.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_pay

## Supported Chains
sui (mainnet)

## Method
`unsafe_pay`

## Parameters
Array of 5 items:

1. **signer** (`string`, required): The transaction signer's Sui address.

2. **input_coins** (`array` of `string`, required): Array of coin object IDs to use as input for the payment.

3. **recipients** (`array` of `string`, required): Array of recipient Sui addresses.

4. **amounts** (`array` of `string`, required): Array of amounts (in MIST) to send to each corresponding recipient.

5. **gas** (`string` | `null`, optional): The gas object ID to use for payment. Must not overlap with `input_coins`. If `null`, the system selects automatically.

6. **gas_budget** (`string`, required): The gas budget for the transaction in MIST.

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
  "method": "unsafe_pay",
  "params": [
    "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3",
    [
      "0xa1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0"
    ],
    [
      "0x1234567890abcdef1234567890abcdef12345678"
    ],
    [
      "1000000000"
    ],
    null,
    "10000000"
  ]
}
```
