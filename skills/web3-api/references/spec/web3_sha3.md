# web3_sha3

> Returns the Keccak-256 hash of the given data. Used for data integrity verification and generating unique identifiers.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/web3_sha3

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`web3_sha3`

## Parameters
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `params` | `array` | Yes | Array of 1 item |
| `params[0]` - Data | `string` | Yes | The data to hash, as a hex-encoded string with `0x` prefix. For example, `"0x68656c6c6f204e4f444954"` represents `"hello NODIT"` |

## Returns
The Keccak-256 hash of the given data as a 64-character hex string (e.g., `"0x274020d2b9b210b079f3898f94123f710f5ab65525f23c7ad9e04e425d3648bd"`).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "web3_sha3",
  "params": [
    "0x68656c6c6f204e4f444954"
  ]
}
```
