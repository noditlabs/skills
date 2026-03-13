# sui-unsafe_payAllSui

> Creates an unsigned transaction to send all SUI from the input coins to a single recipient. The first coin in the list is used for gas, and all remaining coins are merged and sent.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_payAllSui

## Supported Chains
sui (mainnet)

## Method
`unsafe_payAllSui`

## Parameters
Array of 4 items:

1. **signer** (`string`, required): The transaction signer's Sui address.

2. **input_coins** (`array` of `string`, required): Array of SUI coin object IDs. The first coin is used for gas payment.

3. **recipient** (`string`, required): The recipient's Sui address to receive all SUI.

4. **gas_budget** (`string`, required): The gas budget for the transaction in MIST.

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
  "method": "unsafe_payAllSui",
  "params": [
    "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3",
    [
      "0xa1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0",
      "0xf0e1d2c3b4a5f6e7d8c9b0a1f2e3d4c5b6a7f8e9"
    ],
    "0x1234567890abcdef1234567890abcdef12345678",
    "10000000"
  ]
}
```
