# sui-suix_resolveNameServiceNames

> Resolves a Sui address to its associated SuiNS (Sui Name Service) names, with pagination support.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_resolveNameServiceNames

## Supported Chains
sui (mainnet)

## Method
`suix_resolveNameServiceNames`

## Parameters
Array of 3 items:

1. **address** (`string`, required): The Sui address to look up SuiNS names for.

2. **cursor** (`string` | `null`, optional): Paging cursor. Default: `null`.

3. **limit** (`integer` | `null`, optional): Maximum number of items per page.

## Returns
- **NamesPage** (`object`): Paginated list of SuiNS names.
  - `data` (`array`): Array of name strings (e.g., `["example.sui"]`).
  - `nextCursor` (`string` | `null`): Cursor for the next page.
  - `hasNextPage` (`boolean`): Whether more results are available.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_resolveNameServiceNames",
  "params": [
    "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3",
    null,
    10
  ]
}
```
