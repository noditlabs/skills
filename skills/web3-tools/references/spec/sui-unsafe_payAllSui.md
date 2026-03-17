# sui-unsafe_payAllSui

> unsafe_payAllSui

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_payAllSui

## Supported Chains

Sui (mainnet, testnet)

## Method

`unsafe_payAllSui`

## Parameters

Array of parameters:

1. **signer** (`any` (required)): The transaction signer's Sui address
2. **input_coins** (`array` (required)): The Sui coins to be used in this transaction, including the coin for gas payment.
3. **recipient** (`any` (required)): The recipient address
4. **gas_budget** (`any` (required)): The gas budget, the transaction will fail if the gas cost exceed the budget

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
  "method": "unsafe_payAllSui"
}
```
