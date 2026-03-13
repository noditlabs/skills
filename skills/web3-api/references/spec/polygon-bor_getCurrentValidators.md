# polygon-bor_getCurrentValidators

> Returns the list of currently active validators on the Polygon network, providing important information for understanding network governance and security.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/polygon-bor_getCurrentValidators

## Supported Chains
- Polygon

## Method
`bor_getCurrentValidators`

## Parameters
None. This method takes no parameters.

## Returns
An array of validator objects, each containing:
- `ID` (`integer`): Validator ID
- `signer` (`string`): Validator signer address
- `power` (`integer`): Voting power of the validator
- `accum` (`integer`): Accumulator value for proposer selection

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "bor_getCurrentValidators"
}
```
