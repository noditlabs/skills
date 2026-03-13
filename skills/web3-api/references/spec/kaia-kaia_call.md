# kaia-kaia_call

> Executes a smart contract read method without creating a transaction. No state changes occur.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_call

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_call`

## Parameters
- **Call Object** (`object`):
  - `from` (`string`, optional): Sender address.
  - `to` (`string`): Target contract address.
  - `gas` (`string`, optional): Gas limit in hex.
  - `gasPrice` (`string`, optional): Gas price in hex.
  - `value` (`string`, optional): Value to send in hex.
  - `data` (`string`, optional): ABI-encoded method call data.
- **Block Identifier** (`string`): Block number (hex, e.g. `"0x1"`), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).
- **State Override Set** (`object`, optional): Override account balance, nonce, code, state, or stateDiff for simulation.

## Returns
- **result** (`string`): Hex-encoded return data from the contract call.
