# sui-sui_devInspectTransactionBlock

> sui_devInspectTransactionBlock

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_devInspectTransactionBlock

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_devInspectTransactionBlock`

## Parameters

Array of parameters:

1. **sender_address** (`any` (required)): 
2. **tx_bytes** (`any` (required)): BCS encoded TransactionKind(as opposed to TransactionData, which include gasBudget and gasPrice)
3. **gas_price** (`any` (optional)): Gas is not charged, but gas usage is still calculated. Default to use reference gas price
4. **epoch** (`any` (optional)): The epoch to perform the call. Will be set from the system state object if not provided
5. **additional_args** (`any` (optional)): Additional arguments including gas_budget, gas_objects, gas_sponsor and skip_checks.

## Returns

An object containing:
- `effects` (any): 
- `error` (string): Execution error from executing the transactions
- `events` (array): Events that likely would be generated if the transaction is actually run.
- `rawEffects` (array): The raw effects of the transaction that was dev inspected.
- `rawTxnData` (array): The raw transaction data of the transaction that was dev inspected.
- `results` (array): Execution results (including return values) from executing the transactions

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_devInspectTransactionBlock",
  "params": [
    "0xd70420418b84502e506794227f897237764dde8d79a01ab2104bf742a277a2ab",
    "AAACACBnxtMcbJcOVn8D72fYEaT4Q2ZbjePygvpIs+AQO6m77QEAagYVO5/EhuEB8OnicDrIZm0GrsxN3355JqNhlwxlpbECAAAAAAAAACDoQ3EipycU+/EOvBcDPFtMkZiSbdzWAw3CwdmQCAtBWAEBAQEBAAEAAC9cVD1xauQ9RT3rOxmbva8bxwMMdoL4dwPc5DEkj+3gASxDgF0Nb1QCp60Npb3sVJx83qBrxKHTOaIlIe6pM7iJAgAAAAAAAAAgnvsgc1pPauyCE27/c+aBnHN3fSsxRAWdEJYzYFOryNAvXFQ9cWrkPUU96zsZm72vG8cDDHaC+HcD3OQxJI/t4AoAAAAAAAAAoIYBAAAAAAAA",
    1000,
    8888,
    null
  ]
}
```
