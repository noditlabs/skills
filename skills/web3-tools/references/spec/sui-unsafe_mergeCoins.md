# sui-unsafe_mergeCoins

> unsafe_mergeCoins

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`unsafe_mergeCoins`

## Parameters

Array of parameters:

1. **signer** (`any` (required)): The transaction signer's Sui address
2. **primary_coin** (`any` (required)): The coin object to merge into, this coin will remain after the transaction
3. **coin_to_merge** (`any` (required)): The coin object to be merged, this coin will be destroyed, the balance will be added to primary_coin
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
  "method": "unsafe_mergeCoins"
}
```
