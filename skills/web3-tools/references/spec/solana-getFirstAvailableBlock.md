# solana-getFirstAvailableBlock

> getFirstAvailableBlock

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getFirstAvailableBlock`

## Parameters

None - this method takes no parameters.

## Returns

- **result** (`integer`): The slot of the lowest confirmed block that has not been purged from the ledger

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getFirstAvailableBlock"
}
```
