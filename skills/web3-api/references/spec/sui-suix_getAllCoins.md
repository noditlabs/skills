# sui-suix_getAllCoins

> Return all Coin objects owned by an address.

- **Category**: Node API - Sui (JSON-RPC) / Coin Query API
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getAllCoins

## Supported Chains
sui

## Method
`suix_getAllCoins`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | `SuiAddress` | required | the owner's Sui address |
| `cursor` | `string` | optional | optional paging cursor |
| `limit` | `integer` | optional | maximum number of items per page |

## Returns
`Page_for_Coin_and_String` - CoinPage

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getAllCoins",
  "params": [
    "0x94f1a597b4e8f709a396f7f6b1482bdcd65a673d111e49286c527fab7c2d0961"
  ]
}
```
