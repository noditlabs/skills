# sui-sui_getCheckpoints

> sui_getCheckpoints

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_getCheckpoints`

## Parameters

Array of parameters:

1. **cursor** (`any` (required)): An optional paging cursor. If provided, the query will start from the next item after the specified cursor. Default to start from the first item if not specified.
2. **limit** (`integer` (optional)): Maximum item returned per page, default to [QUERY_MAX_RESULT_LIMIT_CHECKPOINTS] if not specified.
3. **descending_order** (`boolean` (optional)): Query result ordering, default to false (ascending order), oldest record first.

## Returns

An object containing:
- `data` (array): 
- `hasNextPage` (boolean): 
- `nextCursor` (string): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getCheckpoints",
  "params": [
    "1004",
    4,
    false
  ]
}
```
