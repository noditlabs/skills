# optimism-optimism_outputAtBlock

> Retrieve the output root at a specific block number. The output root is an important element representing the state of Optimism and can be used to verify the state of a specific block.

- **Category**: Node API - Optimism (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/optimism-optimism_outputAtBlock

## Supported Chains
optimism

## Method
`optimism_outputAtBlock`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `blockNumber` | `string` | required | The block number in hexadecimal format (e.g., "0x1234") to retrieve the output root for. |

## Returns
`object` - OutputResponse containing:
- `outputRoot` (`string`): The output root hash representing the L2 state at the given block.
- `version` (`string`): The version of the output root.
- `blockRef` (`object`): Reference to the L2 block including `blockHash` and `blockNumber`.
- `status` (`integer`): The status code of the output.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "optimism_outputAtBlock",
  "params": [
    "0x123"
  ]
}
```
