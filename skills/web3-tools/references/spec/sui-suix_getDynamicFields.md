# sui-suix_getDynamicFields

> suix_getDynamicFields

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getDynamicFields`

## Parameters

Array of parameters:

1. **parent_object_id** (`any` (required)): The ID of the parent object
2. **cursor** (`any` (optional)): An optional paging cursor. If provided, the query will start from the next item after the specified cursor. Default to start from the first item if not specified.
3. **limit** (`integer` (optional)): Maximum item returned per page, default to [QUERY_MAX_RESULT_LIMIT] if not specified.

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
  "method": "suix_getDynamicFields",
  "params": [
    "0x5612581eba57ebe7e594b809ccceec2be4dac6ff6945d49b3ecc043d049611f6",
    "0x671832358f25bfacde706e528df4e15bb8de6dadd21835dfe44f4973139c15f9",
    3
  ]
}
```
