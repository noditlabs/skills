# sui-unsafe_transferSui

> unsafe_transferSui

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_transferSui

## Supported Chains

Sui (mainnet, testnet)

## Method

`unsafe_transferSui`

## Parameters

Array of parameters:

1. **signer** (`any` (required)): The transaction signer's Sui address
2. **sui_object_id** (`any` (required)): The Sui coin object to be used in this transaction
3. **gas_budget** (`any` (required)): The gas budget, the transaction will fail if the gas cost exceed the budget
4. **recipient** (`any` (required)): The recipient's Sui address
5. **amount** (`any` (optional)): The amount to be split out and transferred

## Returns

An object containing:
- `gas` (array): the gas objects to be used
- `inputObjects` (array): objects to be used in this transaction
- `txBytes` (string): BCS serialized transaction data bytes without its type tag, as base-64 encoded string.

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "unsafe_transferSui"
}
```
