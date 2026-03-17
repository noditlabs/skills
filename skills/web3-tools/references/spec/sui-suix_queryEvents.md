# sui-suix_queryEvents

> suix_queryEvents

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_queryEvents

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_queryEvents`

## Parameters

Array of parameters:

1. **query** (`any` (required)): The event query criteria. See Event filter documentation for examples.
2. **cursor** (`any` (optional)): Optional paging cursor
3. **limit** (`integer` (optional)): Maximum number of items per page, default to [QUERY_MAX_RESULT_LIMIT] if not specified.
4. **descending_order** (`boolean` (optional)): Query result ordering, default to false (ascending order), oldest record first.

## Returns

An object containing:
- `data` (array): 
- `hasNextPage` (boolean): 
- `nextCursor` (object): Unique ID of a Sui Event, the ID is a combination of transaction digest and event seq number.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_queryEvents",
  "params": [
    {
      "MoveModule": {
        "package": "0xa395759ca37c6e1ffc179184e98a6f9a2da5d78f6e34b0e5044ed52a6bc0a1bc",
        "module": "test"
      }
    },
    {
      "txDigest": "Eg3ynETJfTfPKyvJzq3VLG6MngURYHPMjjUJ3Xt1t7tf",
      "eventSeq": "1"
    },
    100,
    false
  ]
}
```
