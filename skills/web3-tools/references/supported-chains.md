# Supported Chains

Chain-by-chain API support summary.

## Overview

| Chain | Node API | Data API | Webhook API |
|-------|----------|----------|-------------|
| aptos | Yes | Yes | Yes |
| arbitrum | Yes | Yes | Yes |
| arc | Yes | Yes | Yes |
| avalanche | Yes | No | No |
| base | Yes | Yes | Yes |
| bitcoin | No | Yes | No |
| bitcoincash | No | Yes | No |
| bnb | Yes | Yes | Yes |
| chiliz | No | Yes | No |
| dogecoin | No | Yes | No |
| ethereum | Yes | Yes | Yes |
| ethereumclassic | No | Yes | No |
| giwa | Yes | Yes | Yes |
| kaia | Yes | Yes | Yes |
| luniverse | Yes | Yes | No |
| optimism | Yes | Yes | Yes |
| polygon | Yes | Yes | Yes |
| solana | Yes | No | No |
| sui | Yes | No | No |
| tron | No | Yes | No |
| xrpl | No | Yes | No |

## Chain Details

### Aptos

**Networks**: mainnet, testnet

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `accounts` | 6 |
| `blocks` | 2 |
| `events` | 2 |
| `general` | 1 |
| `tables` | 2 |
| `transactions` | 11 |
| `view` | 1 |

**Data API**: blockchain, stats, token

**Webhook API** (type: aptos): createWebhook, deleteWebhook, getWebhook, getWebhookHistory, updateWebhook

### Arbitrum

**Networks**: mainnet, sepolia

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `debug` | 4 |
| `eth` | 34 |
| `net` | 1 |
| `web3` | 2 |

**Data API**: blockchain, native, nft, stats, token

**Webhook API** (type: evm): createWebhook, deleteWebhook, getWebhook, getWebhookHistory, updateWebhook

### Arc

**Networks**: testnet

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `debug` | 4 |
| `eth` | 34 |
| `net` | 1 |
| `web3` | 2 |

**Data API**: blockchain, native, nft, stats, token

**Webhook API** (type: evm): createWebhook, deleteWebhook, getWebhook, getWebhookHistory, updateWebhook

### Avalanche

**Networks**: mainnet, fuji

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `debug` | 4 |
| `eth` | 33 |
| `net` | 2 |
| `web3` | 2 |

### Base

**Networks**: mainnet, sepolia

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `debug` | 4 |
| `eth` | 34 |
| `net` | 2 |
| `op-stack` | 2 |
| `web3` | 2 |

**Data API**: blockchain, native, nft, stats, token

**Webhook API** (type: evm): createWebhook, deleteWebhook, getWebhook, getWebhookHistory, updateWebhook

### Bitcoin

**Data API**: blockchain, native

### Bitcoincash

**Data API**: blockchain, native

### Bnb

**Networks**: mainnet, testnet

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `debug` | 4 |
| `eth` | 34 |
| `net` | 2 |
| `web3` | 2 |

**Data API**: blockchain, native, nft, stats, token

**Webhook API** (type: evm): createWebhook, deleteWebhook, getWebhook, getWebhookHistory, updateWebhook

### Chiliz

**Data API**: blockchain, native, nft, stats, token

### Dogecoin

**Data API**: blockchain, native

### Ethereum

**Networks**: mainnet, sepolia, hoodi

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `debug` | 4 |
| `eth` | 34 |
| `net` | 2 |
| `trace` | 7 |
| `web3` | 2 |

**Data API**: blockchain, ens, native, nft, stats, token

**Webhook API** (type: evm): createWebhook, deleteWebhook, getWebhook, getWebhookHistory, updateWebhook

### Ethereumclassic

**Data API**: blockchain, native, nft, stats, token

### Giwa

**Networks**: sepolia

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `debug` | 4 |
| `eth` | 34 |
| `net` | 2 |
| `op-stack` | 2 |
| `web3` | 2 |

**Data API**: blockchain, native, nft, stats, token

**Webhook API** (type: evm): createWebhook, deleteWebhook, getWebhook, getWebhookHistory, updateWebhook

### Kaia

**Networks**: mainnet, kairos

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `debug` | 4 |
| `eth` | 34 |
| `kaia` | 31 |
| `klay` | 30 |
| `net` | 2 |
| `web3` | 2 |

**Data API**: blockchain, native, nft, stats, token

**Webhook API** (type: evm): createWebhook, deleteWebhook, getWebhook, getWebhookHistory, updateWebhook

### Luniverse

**Networks**: mainnet

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `debug` | 4 |
| `eth` | 33 |
| `net` | 2 |
| `web3` | 2 |

**Data API**: blockchain, native, nft, stats, token

### Optimism

**Networks**: mainnet, sepolia

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `debug` | 4 |
| `eth` | 34 |
| `net` | 2 |
| `op-stack` | 2 |
| `web3` | 2 |

**Data API**: blockchain, native, nft, stats, token

**Webhook API** (type: evm): createWebhook, deleteWebhook, getWebhook, getWebhookHistory, updateWebhook

### Polygon

**Networks**: mainnet, amoy

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `bor` | 4 |
| `debug` | 4 |
| `eth` | 33 |
| `net` | 2 |
| `web3` | 2 |

**Data API**: blockchain, native, nft, stats, token

**Webhook API** (type: evm): createWebhook, deleteWebhook, getWebhook, getWebhookHistory, updateWebhook

### Solana

**Networks**: mainnet, devnet

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `http` | 48 |

### Sui

**Networks**: mainnet, testnet

**Node API** (JSON-RPC):

| Namespace | Methods |
|-----------|---------|
| `sui` | 22 |
| `suix` | 21 |
| `unsafe` | 13 |

### Tron

**Data API**: asset, blockchain, native, stats, token

### Xrpl

**Data API**: blockchain, native, token
