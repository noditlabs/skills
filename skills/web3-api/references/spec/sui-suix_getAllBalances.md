# sui-suix_getAllBalances

> Return the total coin balance for all coin type, owned by the address owner.

- **Category**: Node API - Sui (JSON-RPC) / Coin Query API
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getAllBalances

## Supported Chains
sui

## Method
`suix_getAllBalances`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | `SuiAddress` | required | the owner's Sui address |

## Returns
`array` - Vec<Balance>

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getAllBalances",
  "params": [
    "0x94f1a597b4e8f709a396f7f6b1482bdcd65a673d111e49286c527fab7c2d0961"
  ]
}
```
