# sui-unsafe_requestAddStake

> unsafe_requestAddStake

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`unsafe_requestAddStake`

## Parameters

Array of parameters:

1. **signer** (`any` (required)): The transaction signer's Sui address
2. **coins** (`array` (required)): Coin<SUI> object to stake
3. **amount** (`any` (required)): Stake amount
4. **validator** (`any` (required)): The validator's Sui address
5. **gas** (`any` (optional)): Gas object to be used in this transaction, node will pick one from the signer's possession if not provided
6. **gas_budget** (`any` (optional)): The gas budget, the transaction will fail if the gas cost exceed the budget

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
  "method": "unsafe_requestAddStake"
}
```
