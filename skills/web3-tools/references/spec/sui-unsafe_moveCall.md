# sui-unsafe_moveCall

> unsafe_moveCall

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`unsafe_moveCall`

## Parameters

Array of parameters:

1. **signer** (`any` (required)): The transaction signer's Sui address
2. **package_object_id** (`any` (required)): The Move package ID, e.g. 0x2
3. **module** (`string` (required)): The Move module name, e.g. pay
4. **function** (`string` (required)): The move function name, e.g. split
5. **type_arguments** (`array` (required)): The type arguments of the Move function
6. **arguments** (`array` (required)): The arguments to be passed into the Move function, in SuiJson format
7. **gas** (`any` (required)): Gas object to be used in this transaction, node will pick one from the signer's possession if not provided
8. **gas_budget** (`any` (optional)): The gas budget, the transaction will fail if the gas cost exceed the budget
9. **execution_mode** (`any` (optional)): Whether this is a Normal transaction or a Dev Inspect Transaction. Default to be SuiTransactionBlockBuilderMode::Commit when it's None.

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
  "method": "unsafe_moveCall"
}
```
