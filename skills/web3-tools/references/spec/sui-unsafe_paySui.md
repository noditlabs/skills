# sui-unsafe_paySui

> unsafe_paySui

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_paySui

## Supported Chains

Sui (mainnet, testnet)

## Method

`unsafe_paySui`

## Parameters

Array of parameters:

1. **signer** (`any` (required)): The transaction signer's Sui address
2. **input_coins** (`array` (required)): The Sui coins to be used in this transaction, including the coin for gas payment.
3. **recipients** (`array` (required)): The recipients' addresses, the length of this vector must be the same as amounts.
4. **amounts** (`array` (required)): The amounts to be transferred to recipients, following the same order
5. **gas_budget** (`any` (required)): The gas budget, the transaction will fail if the gas cost exceed the budget

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
  "method": "unsafe_paySui"
}
```
