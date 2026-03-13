# sui-unsafe_transferSui

> Creates an unsigned transaction to send SUI from one address to another. The SUI coin object is used for both the transfer and gas payment.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_transferSui

## Supported Chains
sui (mainnet)

## Method
`unsafe_transferSui`

## Parameters
Array of 5 items:

1. **signer** (`string`, required): The transaction signer's Sui address.

2. **sui_object_id** (`string`, required): The SUI coin object ID to transfer from. This coin is also used for gas payment.

3. **recipient** (`string`, required): The recipient's Sui address.

4. **amount** (`string` | `null`, optional): The amount of SUI to transfer in MIST. If `null`, the entire coin is transferred.

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
  "method": "unsafe_transferSui",
  "params": [
    "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3",
    "0xa1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0",
    "0x1234567890abcdef1234567890abcdef12345678",
    "1000000000",
    "10000000"
  ]
}
```
