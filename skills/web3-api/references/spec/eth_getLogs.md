# eth_getLogs

> Returns logs matching the given filter criteria. Unlike eth_getFilterLogs, this method accepts filter conditions directly in the request without requiring a pre-created filter. Keep block ranges to 1000 blocks or fewer for optimal performance.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getLogs

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getLogs`

## Parameters
Array of exactly 1 item:

1. **Log Filter Object** (`object`):
   - `fromBlock` (`string`, optional): Start block number (hex) or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).
   - `toBlock` (`string`, optional): End block number (hex) or block tag.
   - `address` (`array` of `string`, optional): Array of contract addresses to filter (20-byte hex strings).
   - `topics` (`array` of `string`, optional): Array of up to 4 topic values (32-byte hex strings) to filter logs by event signatures and indexed parameters.

## Returns
Array of log objects, each containing:
- **address** (`string`): Contract address that emitted the log.
- **topics** (`array`): Array of 32-byte topic hex strings.
- **data** (`string`): The log data in hex.
- **blockNumber** (`string`): Block number in hex.
- **transactionHash** (`string`): Transaction hash.
- **transactionIndex** (`string`): Transaction index in hex.
- **blockHash** (`string`): Block hash.
- **logIndex** (`string`): Log index in hex.
- **removed** (`boolean`): `true` if the log was removed due to a chain reorganization.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getLogs",
  "params": [
    {
      "fromBlock": "latest"
    }
  ]
}
```
