# sui-sui_dryRunTransactionBlock

> sui_dryRunTransactionBlock

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_dryRunTransactionBlock

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_dryRunTransactionBlock`

## Parameters

Array of parameters:

1. **tx_bytes** (`any` (required)): 

## Returns

An object containing:
- `balanceChanges` (array): 
- `effects` (any): 
- `events` (array): 
- `executionErrorSource` (string): 
- `input` (any): 
- `objectChanges` (array): 
- `suggestedGasPrice` (string): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_dryRunTransactionBlock",
  "params": [
    "AAACACB7qR3cfnF89wjJNwYPBASHNuwz+xdG2Zml5YzVxnftgAEAT4LxyFh7mNZMAL+0bDhDvYv2zPp8ZahhOGmM0f3Kw9wCAAAAAAAAACCxDABG4pPAjOwPQHg9msS/SrtNf4IGR/2F0ZGD3ufH/wEBAQEBAAEAAGH7tbTzQqQL2/h/5KlGueONGM+P/HsAALl1F1x7apV2AejYx86GPzE9o9vZKoPvJtEouI/ma/JuDg0Jza9yfR2EAgAAAAAAAAAgzMqpegLMOpgEFnDhYJ23FOmFjJbp5GmFXxzzv9+X6GVh+7W080KkC9v4f+SpRrnjjRjPj/x7AAC5dRdce2qVdgoAAAAAAAAAoIYBAAAAAAAA"
  ]
}
```
