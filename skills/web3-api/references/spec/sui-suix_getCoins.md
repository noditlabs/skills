# sui-suix_getCoins

> Return all Coin<`coin_type`> objects owned by an address.

- **Category**: Node API - Sui (JSON-RPC) / Coin Query API
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getCoins

## Supported Chains
sui

## Method
`suix_getCoins`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | `SuiAddress` | required | the owner's Sui address |
| `coin_type` | `string` | optional | optional type name for the coin (e.g., 0x168da5bf1f48dafc111b0a488fa454aca95e0b5e::usdc::USDC), default to 0x2::sui::SUI if not specified. |
| `cursor` | `string` | optional | optional paging cursor |
| `limit` | `integer` | optional | maximum number of items per page |

## Returns
`Page_for_Coin_and_String` - CoinPage

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getCoins",
  "params": [
    "0x94f1a597b4e8f709a396f7f6b1482bdcd65a673d111e49286c527fab7c2d0961"
  ]
}
```
