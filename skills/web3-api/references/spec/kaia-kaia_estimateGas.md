# kaia-kaia_estimateGas

> Estimates the gas required to execute a transaction without sending it.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_estimateGas

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_estimateGas`

## Parameters
- **Call Object** (`object`):
  - `from` (`string`, optional): Sender address.
  - `to` (`string`): Target contract address.
  - `gas` (`string`, optional): Gas limit in hex.
  - `gasPrice` (`string`, optional): Gas price in hex.
  - `value` (`string`, optional): Value to send in hex.
  - `data` (`string`, optional): ABI-encoded method call data.

## Returns
- **gasEstimate** (`string`): Estimated gas amount as a hex string.
