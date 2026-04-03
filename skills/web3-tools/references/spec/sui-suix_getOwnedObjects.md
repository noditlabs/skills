# sui-suix_getOwnedObjects

> suix_getOwnedObjects

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getOwnedObjects`

## Parameters

Array of parameters:

1. **address** (`any` (required)): Sui address.
2. **query** (`any` (optional)): The objects query criteria.
3. **cursor** (`any` (optional)): An optional paging cursor. If provided, the query will start from the next item after the specified cursor. Default to start from the first item if not specified.
4. **limit** (`integer` (optional)): Max number of items returned per page, default to [QUERY_MAX_RESULT_LIMIT] if not specified.

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
  "method": "suix_getOwnedObjects",
  "params": [
    "0xdbc9abc01a87906b033a75750e741edb2df5ea5d55c96a611371d22799d26827",
    {
      "filter": {
        "MatchAll": [
          {
            "StructType": "0x2::coin::Coin<0x2::sui::SUI>"
          },
          {
            "AddressOwner": "0xdbc9abc01a87906b033a75750e741edb2df5ea5d55c96a611371d22799d26827"
          },
          {
            "Version": "13488"
          }
        ]
      },
      "options": {
        "showType": true,
        "showOwner": true,
        "showPreviousTransaction": true,
        "showDisplay": false,
        "showContent": false,
        "showBcs": false,
        "showStorageRebate": false
      }
    },
    "0x0cd4bb4d4f520fe9bbf0cf1cebe3f2549412826c3c9261bff9786c240123749f",
    3
  ]
}
```
