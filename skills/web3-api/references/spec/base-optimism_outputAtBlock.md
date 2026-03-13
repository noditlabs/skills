# base-optimism_outputAtBlock

> Retrieves the output root at a specific block, used to verify the Optimism state at that block

- **Category**: Node API - Base (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/base-optimism_outputAtBlock

## Supported Chains
Base (mainnet, sepolia)

## Method
`optimism_outputAtBlock`

## Parameters
| Position | Name | Type | Required | Description |
|----------|------|------|----------|-------------|
| 1 | `blockNumber` | `string` | Yes | Block number as a hex string (e.g., `"0x7C664D5"`). Only the latest 128 blocks can be queried. |

## Returns
An array of two hex strings representing the output root values for the specified block.
