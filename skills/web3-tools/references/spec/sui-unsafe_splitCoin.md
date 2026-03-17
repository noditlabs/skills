# sui-unsafe_splitCoin

> unsafe_splitCoin

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_splitCoin

## Supported Chains

Sui (mainnet, testnet)

## Method

`unsafe_splitCoin`

## Parameters

Array of parameters:

1. **signer** (`any` (required)): The transaction signer's Sui address
2. **coin_object_id** (`any` (required)): The coin object to be spilt
3. **split_amounts** (`array` (required)): The amounts to split out from the coin
4. **gas** (`any` (required)): Gas object to be used in this transaction, node will pick one from the signer's possession if not provided
5. **gas_budget** (`any` (optional)): The gas budget, the transaction will fail if the gas cost exceed the budget

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
  "method": "unsafe_splitCoin"
}
```
