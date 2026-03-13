# polygon-bor_getCurrentProposer

> Returns the address of the current block proposer (the validator responsible for producing the next block) on the Polygon PoA network.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/polygon-bor_getCurrentProposer

## Supported Chains
- Polygon

## Method
`bor_getCurrentProposer`

## Parameters
None. This method takes no parameters.

## Returns
- `result` (`string`): The address of the current block proposer.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "bor_getCurrentProposer"
}
```
