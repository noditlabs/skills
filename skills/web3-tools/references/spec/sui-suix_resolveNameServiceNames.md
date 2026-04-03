# sui-suix_resolveNameServiceNames

> suix_resolveNameServiceNames

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_resolveNameServiceNames`

## Parameters

Array of parameters:

1. **address** (`any` (required)): The address to resolve
2. **cursor** (`any` (optional)): Optional paging cursor
3. **limit** (`integer` (optional)): Maximum number of items per page

## Returns

An object containing:
- `data` (array): 
- `hasNextPage` (boolean): 
- `nextCursor` (string): hexadecimal string encoding.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_resolveNameServiceNames",
  "params": [
    "0x5cd6fa76ed1d18f05f15e35075252ddec4fb83621d55952d9172fcfcb72feae2",
    "0xd22bbb46f892c42d9ec0ae4de93e02c75973a51c17180798237326a58694a2cf",
    3
  ]
}
```
