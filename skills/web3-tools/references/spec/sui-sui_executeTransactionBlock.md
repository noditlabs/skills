# sui-sui_executeTransactionBlock

> sui_executeTransactionBlock

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_executeTransactionBlock`

## Parameters

Array of parameters:

1. **tx_bytes** (`any` (required)): 
2. **signatures** (`array` (required)): 
3. **options** (`any` (optional)): 
4. **request_type** (`string` (optional)): 

## Returns

An object containing:
- `balanceChanges` (['array', 'null']): 
- `checkpoint` (string): 
- `confirmedLocalExecution` (['boolean', 'null']): 
- `digest` (object): A representation of a 32 byte digest
- `effects` (any): 
- `errors` (array): 
- `events` (['array', 'null']): 
- `objectChanges` (['array', 'null']): 
- `rawEffects` (array): 
- `rawTransaction` (string): Base64 encoding.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_executeTransactionBlock",
  "params": [
    "AAACACBqEB6aOvXIBwES+Ahkizbvv43uihqC3kbZUE6WoRCKFwEAjvdvVsOZYzousxC8qRJOXy84znOeqsu2YAaIgE4HhEgCAAAAAAAAACB9w3+ufZMpihJFwxtCBojBaGy00TVtFxgN2C6TpIPFqwEBAQEBAAEAAAS0l6kWtGVmCaf6gnoJGE1vR2gdO6dM4NejbGSysfiHAZ+Q9/hmzCnfsdpjc86U+dldylpA9OF2mRjuv5+64AvTAgAAAAAAAAAgjleHL0UiRGjh/BfIFHCJ3EMY/dQA22c2TvNQyVJnbYUEtJepFrRlZgmn+oJ6CRhNb0doHTunTODXo2xksrH4hwoAAAAAAAAAoIYBAAAAAAAA",
    [
      "AKD4XdltkCyBi1Heb4EJJ3lzuV3F4u7+CYeaE+Fd7qXpaT17yd4tHWjMf4CWq3TuXBLxTpkc2MV39P6p7eMV8QnqvbuA0Q1Bqu4RHV3JPpqmH+C527hWJGUBOZN1j9sg8w=="
    ],
    {
      "showInput": true,
      "showRawInput": true,
      "showEffects": true,
      "showEvents": true,
      "showObjectChanges": true,
      "showBalanceChanges": true,
      "showRawEffects": false
    },
    "WaitForLocalExecution"
  ]
}
```
