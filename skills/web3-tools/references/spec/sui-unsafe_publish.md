# sui-unsafe_publish

> unsafe_publish

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_publish

## Supported Chains

Sui (mainnet, testnet)

## Method

`unsafe_publish`

## Parameters

Array of parameters:

1. **sender** (`any` (required)): The transaction signer's Sui address
2. **compiled_modules** (`array` (required)): The compiled bytes of a Move package
3. **dependencies** (`array` (required)): A list of transitive dependency addresses that this set of modules depends on.
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
  "method": "unsafe_publish"
}
```
