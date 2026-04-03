# giwa-eth_sendrawtransaction

> eth_sendRawTransaction

- **Category**: Node API - Giwa (JSON-RPC)

## Supported Chains

Giwa (sepolia)

## Method

`eth_sendRawTransaction`

## Parameters

Array of parameters:

1. **Signed Transaction Hash** (`string` (optional)): signature transaction hash signature transaction hashvalue. signature transaction hash 0x hexadecimal string . signature transaction hash . 1. transaction data creation . data , , gas price, gas limit, . 2. transaction data RLP(Recursive Length Prefix) encoding . 3. RLP encoding data Keccak-256 hash function hashvalue creation . 4. creation hashvalue signature . signature hashvalue signature transaction hash.

## Returns

- **result** (`string`): transaction hash transaction . 64 hexadecimal string .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_sendRawTransaction",
  "params": [
    "0x02f8688080808080943f39cfbaff46cb736a603269d14a7e9adf5158b488016345785d8a000080c001a005599173ee4483fa38044e8d7bf592b58a9ab598f7d4a510702d193c60af15a0a00f2d39e8202dc9d7d66a51fc67fcf1d893b20e080c6acf2b25610f5e926cfa21"
  ]
}
```
