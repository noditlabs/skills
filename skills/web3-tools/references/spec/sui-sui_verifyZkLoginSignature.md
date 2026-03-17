# sui-sui_verifyZkLoginSignature

> sui_verifyZkLoginSignature

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_verifyZkLoginSignature

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_verifyZkLoginSignature`

## Parameters

Array of parameters:

1. **bytes** (`string` (required)): The Base64 string of bcs bytes for raw transaction data or personal message indicated by intent_scope.
2. **signature** (`string` (required)): The Base64 string of the zklogin signature to verify.
3. **intent_scope** (`any` (required)): The intent scope, either transaction data or personal message. Used to parse bytes.
4. **author** (`any` (required)): The author of the signature.

## Returns

An object containing:
- `errors` (array): The errors field captures any verification error
- `success` (boolean): The boolean result of the verification. If true, errors should be empty.

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "sui_verifyZkLoginSignature"
}
```
