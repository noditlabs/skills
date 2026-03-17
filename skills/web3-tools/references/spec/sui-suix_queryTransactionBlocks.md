# sui-suix_queryTransactionBlocks

> suix_queryTransactionBlocks

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_queryTransactionBlocks

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_queryTransactionBlocks`

## Parameters

Array of parameters:

1. **query** (`any` (required)): The transaction query criteria.
2. **cursor** (`any` (optional)): An optional paging cursor. If provided, the query will start from the next item after the specified cursor. Default to start from the first item if not specified.
3. **limit** (`integer` (optional)): Maximum item returned per page, default to QUERY_MAX_RESULT_LIMIT if not specified.
4. **descending_order** (`boolean` (optional)): Query result ordering, default to false (ascending order), oldest record first.

## Returns

An object containing:
- `data` (array): 
- `hasNextPage` (boolean): 
- `nextCursor` (object): A representation of a 32 byte digest

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_queryTransactionBlocks",
  "params": [
    {
      "filter": {
        "InputObject": "0x93633829fcba6d6e0ccb13d3dbfe7614b81ea76b255e5d435032cd8595f37eb8"
      },
      "options": null
    },
    "HxidAfFfyr4kXSiWeVq1J6Tk526YUVDoSUY5PSnS4tEJ",
    100,
    false
  ]
}
```
