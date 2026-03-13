# sui-suix_getCoinMetadata

> Return metadata (e.g., symbol, decimals) for a coin. Note that if the coin's metadata was wrapped in the transaction that published its marker type, or the latest version of the metadata object is wrapped or deleted, it will not be found.

- **Category**: Node API - Sui (JSON-RPC) / Coin Query API
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getCoinMetadata

## Supported Chains
sui

## Method
`suix_getCoinMetadata`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `coin_type` | `string` | required | type name for the coin (e.g., 0x168da5bf1f48dafc111b0a488fa454aca95e0b5e::usdc::USDC) |

## Returns
`SuiCoinMetadata` - SuiCoinMetadata

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getCoinMetadata",
  "params": [
    "example_string"
  ]
}
```
