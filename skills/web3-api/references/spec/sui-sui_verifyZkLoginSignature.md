# sui-sui_verifyZkLoginSignature

> Verify a zklogin signature for the given bytes, intent scope and author.

- **Category**: Node API - Sui (JSON-RPC) / Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_verifyZkLoginSignature

## Supported Chains
sui

## Method
`sui_verifyZkLoginSignature`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `bytes` | `string` | required | The Base64 string of bcs bytes for raw transaction data or personal message indicated by intent_scope. |
| `signature` | `string` | required | The Base64 string of the zklogin signature to verify. |
| `intent_scope` | `ZkLoginIntentScope` | required | The intent scope, either transaction data or personal message. Used to parse bytes. |
| `author` | `SuiAddress` | required | The author of the signature. |

## Returns
`ZkLoginVerifyResult` - ZkLoginVerifyResult

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_verifyZkLoginSignature",
  "params": [
    "example_string",
    "example_string",
    "TransactionData",
    "0x94f1a597b4e8f709a396f7f6b1482bdcd65a673d111e49286c527fab7c2d0961"
  ]
}
```
