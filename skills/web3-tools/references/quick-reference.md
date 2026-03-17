# Quick Reference

Complete index of all Nodit API operations, grouped by category.

## operationId Rules

| Source | operationId Format | Example |
|--------|-------------------|---------|
| EVM Node API | `{chain}-{method}` (lowercase) | `ethereum-eth_blocknumber` |
| Solana Node API | `solana-{method}` (camelCase) | `solana-getBalance` |
| Sui Node API | `sui-{method}` | `sui-sui_getLatestCheckpointSequenceNumber` |
| Aptos Node API | `aptos-{method}` (camelCase) | `aptos-getLedgerInfo` |
| Data API | `{method}` (camelCase) | `getTokenAllowance` |
| Webhook API | `{method}` (camelCase) | `createWebhook` |

## Node API - Arbitrum (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `arbitrum-eth_blocknumber` | eth_blockNumber | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_blocknumber.md) |
| `arbitrum-eth_call` | eth_call | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_call.md) |
| `arbitrum-eth_chainid` | eth_chainId | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_chainid.md) |
| `arbitrum-eth_createaccesslist` | eth_createAccessList | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_createaccesslist.md) |
| `arbitrum-eth_estimategas` | eth_estimateGas | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_estimategas.md) |
| `arbitrum-eth_feehistory` | eth_feeHistory | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_feehistory.md) |
| `arbitrum-eth_gasprice` | eth_gasPrice | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_gasprice.md) |
| `arbitrum-eth_getbalance` | eth_getBalance | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getbalance.md) |
| `arbitrum-eth_getblockbyhash` | eth_getBlockByHash | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getblockbyhash.md) |
| `arbitrum-eth_getblockbynumber` | eth_getBlockByNumber | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getblockbynumber.md) |
| `arbitrum-eth_getblockreceipts` | eth_getBlockReceipts | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getblockreceipts.md) |
| `arbitrum-eth_getblocktransactioncountbyhash` | eth_getBlockTransactionCountByHash | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getblocktransactioncountbyhash.md) |
| `arbitrum-eth_getblocktransactioncountbynumber` | eth_getBlockTransactionCountByNumber | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getblocktransactioncountbynumber.md) |
| `arbitrum-eth_getcode` | eth_getCode | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getcode.md) |
| `arbitrum-eth_getfilterchanges` | eth_getFilterChanges | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getfilterchanges.md) |
| `arbitrum-eth_getfilterlogs` | eth_getFilterLogs | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getfilterlogs.md) |
| `arbitrum-eth_getlogs` | eth_getLogs | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getlogs.md) |
| `arbitrum-eth_getproof` | eth_getProof | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getproof.md) |
| `arbitrum-eth_getstorageat` | eth_getStorageAt | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getstorageat.md) |
| `arbitrum-eth_gettransactionbyblockhashandindex` | eth_getTransactionByBlockHashAndIndex | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_gettransactionbyblockhashandindex.md) |
| `arbitrum-eth_gettransactionbyblocknumberandindex` | eth_getTransactionByBlockNumberAndIndex | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_gettransactionbyblocknumberandindex.md) |
| `arbitrum-eth_gettransactionbyhash` | eth_getTransactionByHash | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_gettransactionbyhash.md) |
| `arbitrum-eth_gettransactioncount` | eth_getTransactionCount | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_gettransactioncount.md) |
| `arbitrum-eth_gettransactionreceipt` | eth_getTransactionReceipt | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_gettransactionreceipt.md) |
| `arbitrum-eth_getunclebyblockhashandindex` | eth_getUncleByBlockHashAndIndex | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getunclebyblockhashandindex.md) |
| `arbitrum-eth_getunclebyblocknumberandindex` | eth_getUncleByBlockNumberAndIndex | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getunclebyblocknumberandindex.md) |
| `arbitrum-eth_getunclecountbyblockhash` | eth_getUncleCountByBlockHash | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getunclecountbyblockhash.md) |
| `arbitrum-eth_getunclecountbyblocknumber` | eth_getUncleCountByBlockNumber | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_getunclecountbyblocknumber.md) |
| `arbitrum-eth_maxpriorityfeepergas` | eth_maxPriorityFeePerGas | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_maxpriorityfeepergas.md) |
| `arbitrum-eth_newblockfilter` | eth_newBlockFilter | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_newblockfilter.md) |
| `arbitrum-eth_newfilter` | eth_newFilter | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_newfilter.md) |
| `arbitrum-eth_newpendingtransactionfilter` | eth_newPendingTransactionFilter | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_newpendingtransactionfilter.md) |
| `arbitrum-eth_sendrawtransaction` | eth_sendRawTransaction | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_sendrawtransaction.md) |
| `arbitrum-eth_uninstallfilter` | eth_uninstallFilter | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-eth_uninstallfilter.md) |
| `arbitrum-net_version` | net_version | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-net_version.md) |
| `arbitrum-web3_clientversion` | web3_clientVersion | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-web3_clientversion.md) |
| `arbitrum-web3_sha3` | web3_sha3 | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-web3_sha3.md) |

## Node API - Arbitrum Debug (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `arbitrum-debug_traceblockbyhash` | debug_traceBlockByHash | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-debug_traceblockbyhash.md) |
| `arbitrum-debug_traceblockbynumber` | debug_traceBlockByNumber | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-debug_traceblockbynumber.md) |
| `arbitrum-debug_tracecall` | debug_traceCall | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-debug_tracecall.md) |
| `arbitrum-debug_tracetransaction` | debug_traceTransaction | Arbitrum (mainnet, sepolia) | [spec](spec/arbitrum-debug_tracetransaction.md) |

## Node API - Arc (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `arc-eth_blocknumber` | eth_blockNumber | Arc (testnet) | [spec](spec/arc-eth_blocknumber.md) |
| `arc-eth_call` | eth_call | Arc (testnet) | [spec](spec/arc-eth_call.md) |
| `arc-eth_chainid` | eth_chainId | Arc (testnet) | [spec](spec/arc-eth_chainid.md) |
| `arc-eth_createaccesslist` | eth_createAccessList | Arc (testnet) | [spec](spec/arc-eth_createaccesslist.md) |
| `arc-eth_estimategas` | eth_estimateGas | Arc (testnet) | [spec](spec/arc-eth_estimategas.md) |
| `arc-eth_feehistory` | eth_feeHistory | Arc (testnet) | [spec](spec/arc-eth_feehistory.md) |
| `arc-eth_gasprice` | eth_gasPrice | Arc (testnet) | [spec](spec/arc-eth_gasprice.md) |
| `arc-eth_getbalance` | eth_getBalance | Arc (testnet) | [spec](spec/arc-eth_getbalance.md) |
| `arc-eth_getblockbyhash` | eth_getBlockByHash | Arc (testnet) | [spec](spec/arc-eth_getblockbyhash.md) |
| `arc-eth_getblockbynumber` | eth_getBlockByNumber | Arc (testnet) | [spec](spec/arc-eth_getblockbynumber.md) |
| `arc-eth_getblockreceipts` | eth_getBlockReceipts | Arc (testnet) | [spec](spec/arc-eth_getblockreceipts.md) |
| `arc-eth_getblocktransactioncountbyhash` | eth_getBlockTransactionCountByHash | Arc (testnet) | [spec](spec/arc-eth_getblocktransactioncountbyhash.md) |
| `arc-eth_getblocktransactioncountbynumber` | eth_getBlockTransactionCountByNumber | Arc (testnet) | [spec](spec/arc-eth_getblocktransactioncountbynumber.md) |
| `arc-eth_getcode` | eth_getCode | Arc (testnet) | [spec](spec/arc-eth_getcode.md) |
| `arc-eth_getfilterchanges` | eth_getFilterChanges | Arc (testnet) | [spec](spec/arc-eth_getfilterchanges.md) |
| `arc-eth_getfilterlogs` | eth_getFilterLogs | Arc (testnet) | [spec](spec/arc-eth_getfilterlogs.md) |
| `arc-eth_getlogs` | eth_getLogs | Arc (testnet) | [spec](spec/arc-eth_getlogs.md) |
| `arc-eth_getproof` | eth_getProof | Arc (testnet) | [spec](spec/arc-eth_getproof.md) |
| `arc-eth_getstorageat` | eth_getStorageAt | Arc (testnet) | [spec](spec/arc-eth_getstorageat.md) |
| `arc-eth_gettransactionbyblockhashandindex` | eth_getTransactionByBlockHashAndIndex | Arc (testnet) | [spec](spec/arc-eth_gettransactionbyblockhashandindex.md) |
| `arc-eth_gettransactionbyblocknumberandindex` | eth_getTransactionByBlockNumberAndIndex | Arc (testnet) | [spec](spec/arc-eth_gettransactionbyblocknumberandindex.md) |
| `arc-eth_gettransactionbyhash` | eth_getTransactionByHash | Arc (testnet) | [spec](spec/arc-eth_gettransactionbyhash.md) |
| `arc-eth_gettransactioncount` | eth_getTransactionCount | Arc (testnet) | [spec](spec/arc-eth_gettransactioncount.md) |
| `arc-eth_gettransactionreceipt` | eth_getTransactionReceipt | Arc (testnet) | [spec](spec/arc-eth_gettransactionreceipt.md) |
| `arc-eth_getunclebyblockhashandindex` | eth_getUncleByBlockHashAndIndex | Arc (testnet) | [spec](spec/arc-eth_getunclebyblockhashandindex.md) |
| `arc-eth_getunclebyblocknumberandindex` | eth_getUncleByBlockNumberAndIndex | Arc (testnet) | [spec](spec/arc-eth_getunclebyblocknumberandindex.md) |
| `arc-eth_getunclecountbyblockhash` | eth_getUncleCountByBlockHash | Arc (testnet) | [spec](spec/arc-eth_getunclecountbyblockhash.md) |
| `arc-eth_getunclecountbyblocknumber` | eth_getUncleCountByBlockNumber | Arc (testnet) | [spec](spec/arc-eth_getunclecountbyblocknumber.md) |
| `arc-eth_maxpriorityfeepergas` | eth_maxPriorityFeePerGas | Arc (testnet) | [spec](spec/arc-eth_maxpriorityfeepergas.md) |
| `arc-eth_newblockfilter` | eth_newBlockFilter | Arc (testnet) | [spec](spec/arc-eth_newblockfilter.md) |
| `arc-eth_newfilter` | eth_newFilter | Arc (testnet) | [spec](spec/arc-eth_newfilter.md) |
| `arc-eth_newpendingtransactionfilter` | eth_newPendingTransactionFilter | Arc (testnet) | [spec](spec/arc-eth_newpendingtransactionfilter.md) |
| `arc-eth_sendrawtransaction` | eth_sendRawTransaction | Arc (testnet) | [spec](spec/arc-eth_sendrawtransaction.md) |
| `arc-eth_uninstallfilter` | eth_uninstallFilter | Arc (testnet) | [spec](spec/arc-eth_uninstallfilter.md) |
| `arc-net_version` | net_version | Arc (testnet) | [spec](spec/arc-net_version.md) |
| `arc-web3_clientversion` | web3_clientVersion | Arc (testnet) | [spec](spec/arc-web3_clientversion.md) |
| `arc-web3_sha3` | web3_sha3 | Arc (testnet) | [spec](spec/arc-web3_sha3.md) |

## Node API - Arc Debug (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `arc-debug_traceblockbyhash` | debug_traceBlockByHash | Arc (testnet) | [spec](spec/arc-debug_traceblockbyhash.md) |
| `arc-debug_traceblockbynumber` | debug_traceBlockByNumber | Arc (testnet) | [spec](spec/arc-debug_traceblockbynumber.md) |
| `arc-debug_tracecall` | debug_traceCall | Arc (testnet) | [spec](spec/arc-debug_tracecall.md) |
| `arc-debug_tracetransaction` | debug_traceTransaction | Arc (testnet) | [spec](spec/arc-debug_tracetransaction.md) |

## Node API - Avalanche (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `avalanche-eth_blocknumber` | eth_blockNumber | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_blocknumber.md) |
| `avalanche-eth_call` | eth_call | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_call.md) |
| `avalanche-eth_chainid` | eth_chainId | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_chainid.md) |
| `avalanche-eth_createaccesslist` | eth_createAccessList | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_createaccesslist.md) |
| `avalanche-eth_estimategas` | eth_estimateGas | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_estimategas.md) |
| `avalanche-eth_feehistory` | eth_feeHistory | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_feehistory.md) |
| `avalanche-eth_gasprice` | eth_gasPrice | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_gasprice.md) |
| `avalanche-eth_getbalance` | eth_getBalance | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getbalance.md) |
| `avalanche-eth_getblockbyhash` | eth_getBlockByHash | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getblockbyhash.md) |
| `avalanche-eth_getblockbynumber` | eth_getBlockByNumber | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getblockbynumber.md) |
| `avalanche-eth_getblocktransactioncountbyhash` | eth_getBlockTransactionCountByHash | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getblocktransactioncountbyhash.md) |
| `avalanche-eth_getblocktransactioncountbynumber` | eth_getBlockTransactionCountByNumber | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getblocktransactioncountbynumber.md) |
| `avalanche-eth_getcode` | eth_getCode | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getcode.md) |
| `avalanche-eth_getfilterchanges` | eth_getFilterChanges | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getfilterchanges.md) |
| `avalanche-eth_getfilterlogs` | eth_getFilterLogs | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getfilterlogs.md) |
| `avalanche-eth_getlogs` | eth_getLogs | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getlogs.md) |
| `avalanche-eth_getproof` | eth_getProof | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getproof.md) |
| `avalanche-eth_getstorageat` | eth_getStorageAt | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getstorageat.md) |
| `avalanche-eth_gettransactionbyblockhashandindex` | eth_getTransactionByBlockHashAndIndex | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_gettransactionbyblockhashandindex.md) |
| `avalanche-eth_gettransactionbyblocknumberandindex` | eth_getTransactionByBlockNumberAndIndex | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_gettransactionbyblocknumberandindex.md) |
| `avalanche-eth_gettransactionbyhash` | eth_getTransactionByHash | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_gettransactionbyhash.md) |
| `avalanche-eth_gettransactioncount` | eth_getTransactionCount | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_gettransactioncount.md) |
| `avalanche-eth_gettransactionreceipt` | eth_getTransactionReceipt | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_gettransactionreceipt.md) |
| `avalanche-eth_getunclebyblockhashandindex` | eth_getUncleByBlockHashAndIndex | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getunclebyblockhashandindex.md) |
| `avalanche-eth_getunclebyblocknumberandindex` | eth_getUncleByBlockNumberAndIndex | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getunclebyblocknumberandindex.md) |
| `avalanche-eth_getunclecountbyblockhash` | eth_getUncleCountByBlockHash | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getunclecountbyblockhash.md) |
| `avalanche-eth_getunclecountbyblocknumber` | eth_getUncleCountByBlockNumber | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_getunclecountbyblocknumber.md) |
| `avalanche-eth_maxpriorityfeepergas` | eth_maxPriorityFeePerGas | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_maxpriorityfeepergas.md) |
| `avalanche-eth_newblockfilter` | eth_newBlockFilter | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_newblockfilter.md) |
| `avalanche-eth_newfilter` | eth_newFilter | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_newfilter.md) |
| `avalanche-eth_newpendingtransactionfilter` | eth_newPendingTransactionFilter | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_newpendingtransactionfilter.md) |
| `avalanche-eth_sendrawtransaction` | eth_sendRawTransaction | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_sendrawtransaction.md) |
| `avalanche-eth_uninstallfilter` | eth_uninstallFilter | Avalanche (mainnet, fuji) | [spec](spec/avalanche-eth_uninstallfilter.md) |
| `avalanche-net_listening` | net_listening | Avalanche (mainnet, fuji) | [spec](spec/avalanche-net_listening.md) |
| `avalanche-net_version` | net_version | Avalanche (mainnet, fuji) | [spec](spec/avalanche-net_version.md) |
| `avalanche-web3_clientversion` | web3_clientVersion | Avalanche (mainnet, fuji) | [spec](spec/avalanche-web3_clientversion.md) |
| `avalanche-web3_sha3` | web3_sha3 | Avalanche (mainnet, fuji) | [spec](spec/avalanche-web3_sha3.md) |

## Node API - Avalanche Debug (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `avalanche-debug_traceblockbyhash` | debug_traceBlockByHash | Avalanche (mainnet, fuji) | [spec](spec/avalanche-debug_traceblockbyhash.md) |
| `avalanche-debug_traceblockbynumber` | debug_traceBlockByNumber | Avalanche (mainnet, fuji) | [spec](spec/avalanche-debug_traceblockbynumber.md) |
| `avalanche-debug_tracecall` | debug_traceCall | Avalanche (mainnet, fuji) | [spec](spec/avalanche-debug_tracecall.md) |
| `avalanche-debug_tracetransaction` | debug_traceTransaction | Avalanche (mainnet, fuji) | [spec](spec/avalanche-debug_tracetransaction.md) |

## Node API - Base (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `base-eth_blocknumber` | eth_blockNumber | Base (mainnet, sepolia) | [spec](spec/base-eth_blocknumber.md) |
| `base-eth_call` | eth_call | Base (mainnet, sepolia) | [spec](spec/base-eth_call.md) |
| `base-eth_chainid` | eth_chainId | Base (mainnet, sepolia) | [spec](spec/base-eth_chainid.md) |
| `base-eth_createaccesslist` | eth_createAccessList | Base (mainnet, sepolia) | [spec](spec/base-eth_createaccesslist.md) |
| `base-eth_estimategas` | eth_estimateGas | Base (mainnet, sepolia) | [spec](spec/base-eth_estimategas.md) |
| `base-eth_feehistory` | eth_feeHistory | Base (mainnet, sepolia) | [spec](spec/base-eth_feehistory.md) |
| `base-eth_gasprice` | eth_gasPrice | Base (mainnet, sepolia) | [spec](spec/base-eth_gasprice.md) |
| `base-eth_getbalance` | eth_getBalance | Base (mainnet, sepolia) | [spec](spec/base-eth_getbalance.md) |
| `base-eth_getblockbyhash` | eth_getBlockByHash | Base (mainnet, sepolia) | [spec](spec/base-eth_getblockbyhash.md) |
| `base-eth_getblockbynumber` | eth_getBlockByNumber | Base (mainnet, sepolia) | [spec](spec/base-eth_getblockbynumber.md) |
| `base-eth_getblockreceipts` | eth_getBlockReceipts | Base (mainnet, sepolia) | [spec](spec/base-eth_getblockreceipts.md) |
| `base-eth_getblocktransactioncountbyhash` | eth_getBlockTransactionCountByHash | Base (mainnet, sepolia) | [spec](spec/base-eth_getblocktransactioncountbyhash.md) |
| `base-eth_getblocktransactioncountbynumber` | eth_getBlockTransactionCountByNumber | Base (mainnet, sepolia) | [spec](spec/base-eth_getblocktransactioncountbynumber.md) |
| `base-eth_getcode` | eth_getCode | Base (mainnet, sepolia) | [spec](spec/base-eth_getcode.md) |
| `base-eth_getfilterchanges` | eth_getFilterChanges | Base (mainnet, sepolia) | [spec](spec/base-eth_getfilterchanges.md) |
| `base-eth_getfilterlogs` | eth_getFilterLogs | Base (mainnet, sepolia) | [spec](spec/base-eth_getfilterlogs.md) |
| `base-eth_getlogs` | eth_getLogs | Base (mainnet, sepolia) | [spec](spec/base-eth_getlogs.md) |
| `base-eth_getproof` | eth_getProof | Base (mainnet, sepolia) | [spec](spec/base-eth_getproof.md) |
| `base-eth_getstorageat` | eth_getStorageAt | Base (mainnet, sepolia) | [spec](spec/base-eth_getstorageat.md) |
| `base-eth_gettransactionbyblockhashandindex` | eth_getTransactionByBlockHashAndIndex | Base (mainnet, sepolia) | [spec](spec/base-eth_gettransactionbyblockhashandindex.md) |
| `base-eth_gettransactionbyblocknumberandindex` | eth_getTransactionByBlockNumberAndIndex | Base (mainnet, sepolia) | [spec](spec/base-eth_gettransactionbyblocknumberandindex.md) |
| `base-eth_gettransactionbyhash` | eth_getTransactionByHash | Base (mainnet, sepolia) | [spec](spec/base-eth_gettransactionbyhash.md) |
| `base-eth_gettransactioncount` | eth_getTransactionCount | Base (mainnet, sepolia) | [spec](spec/base-eth_gettransactioncount.md) |
| `base-eth_gettransactionreceipt` | eth_getTransactionReceipt | Base (mainnet, sepolia) | [spec](spec/base-eth_gettransactionreceipt.md) |
| `base-eth_getunclebyblockhashandindex` | eth_getUncleByBlockHashAndIndex | Base (mainnet, sepolia) | [spec](spec/base-eth_getunclebyblockhashandindex.md) |
| `base-eth_getunclebyblocknumberandindex` | eth_getUncleByBlockNumberAndIndex | Base (mainnet, sepolia) | [spec](spec/base-eth_getunclebyblocknumberandindex.md) |
| `base-eth_getunclecountbyblockhash` | eth_getUncleCountByBlockHash | Base (mainnet, sepolia) | [spec](spec/base-eth_getunclecountbyblockhash.md) |
| `base-eth_getunclecountbyblocknumber` | eth_getUncleCountByBlockNumber | Base (mainnet, sepolia) | [spec](spec/base-eth_getunclecountbyblocknumber.md) |
| `base-eth_maxpriorityfeepergas` | eth_maxPriorityFeePerGas | Base (mainnet, sepolia) | [spec](spec/base-eth_maxpriorityfeepergas.md) |
| `base-eth_newblockfilter` | eth_newBlockFilter | Base (mainnet, sepolia) | [spec](spec/base-eth_newblockfilter.md) |
| `base-eth_newfilter` | eth_newFilter | Base (mainnet, sepolia) | [spec](spec/base-eth_newfilter.md) |
| `base-eth_newpendingtransactionfilter` | eth_newPendingTransactionFilter | Base (mainnet, sepolia) | [spec](spec/base-eth_newpendingtransactionfilter.md) |
| `base-eth_sendrawtransaction` | eth_sendRawTransaction | Base (mainnet, sepolia) | [spec](spec/base-eth_sendrawtransaction.md) |
| `base-eth_uninstallfilter` | eth_uninstallFilter | Base (mainnet, sepolia) | [spec](spec/base-eth_uninstallfilter.md) |
| `base-net_listening` | net_listening | Base (mainnet, sepolia) | [spec](spec/base-net_listening.md) |
| `base-net_version` | net_version | Base (mainnet, sepolia) | [spec](spec/base-net_version.md) |
| `base-optimism_outputatblock` | optimism_outputAtBlock | Base (mainnet, sepolia) | [spec](spec/base-optimism_outputatblock.md) |
| `base-optimism_rollupconfig` | optimism_rollupConfig | Base (mainnet, sepolia) | [spec](spec/base-optimism_rollupconfig.md) |
| `base-web3_clientversion` | web3_clientVersion | Base (mainnet, sepolia) | [spec](spec/base-web3_clientversion.md) |
| `base-web3_sha3` | web3_sha3 | Base (mainnet, sepolia) | [spec](spec/base-web3_sha3.md) |

## Node API - Base Debug (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `base-debug_traceblockbyhash` | debug_traceBlockByHash | Base (mainnet, sepolia) | [spec](spec/base-debug_traceblockbyhash.md) |
| `base-debug_traceblockbynumber` | debug_traceBlockByNumber | Base (mainnet, sepolia) | [spec](spec/base-debug_traceblockbynumber.md) |
| `base-debug_tracecall` | debug_traceCall | Base (mainnet, sepolia) | [spec](spec/base-debug_tracecall.md) |
| `base-debug_tracetransaction` | debug_traceTransaction | Base (mainnet, sepolia) | [spec](spec/base-debug_tracetransaction.md) |

## Node API - Bnb (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `bnb-eth_blocknumber` | eth_blockNumber | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_blocknumber.md) |
| `bnb-eth_call` | eth_call | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_call.md) |
| `bnb-eth_chainid` | eth_chainId | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_chainid.md) |
| `bnb-eth_createaccesslist` | eth_createAccessList | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_createaccesslist.md) |
| `bnb-eth_estimategas` | eth_estimateGas | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_estimategas.md) |
| `bnb-eth_feehistory` | eth_feeHistory | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_feehistory.md) |
| `bnb-eth_gasprice` | eth_gasPrice | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_gasprice.md) |
| `bnb-eth_getbalance` | eth_getBalance | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getbalance.md) |
| `bnb-eth_getblockbyhash` | eth_getBlockByHash | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getblockbyhash.md) |
| `bnb-eth_getblockbynumber` | eth_getBlockByNumber | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getblockbynumber.md) |
| `bnb-eth_getblockreceipts` | eth_getBlockReceipts | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getblockreceipts.md) |
| `bnb-eth_getblocktransactioncountbyhash` | eth_getBlockTransactionCountByHash | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getblocktransactioncountbyhash.md) |
| `bnb-eth_getblocktransactioncountbynumber` | eth_getBlockTransactionCountByNumber | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getblocktransactioncountbynumber.md) |
| `bnb-eth_getcode` | eth_getCode | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getcode.md) |
| `bnb-eth_getfilterchanges` | eth_getFilterChanges | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getfilterchanges.md) |
| `bnb-eth_getfilterlogs` | eth_getFilterLogs | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getfilterlogs.md) |
| `bnb-eth_getlogs` | eth_getLogs | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getlogs.md) |
| `bnb-eth_getproof` | eth_getProof | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getproof.md) |
| `bnb-eth_getstorageat` | eth_getStorageAt | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getstorageat.md) |
| `bnb-eth_gettransactionbyblockhashandindex` | eth_getTransactionByBlockHashAndIndex | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_gettransactionbyblockhashandindex.md) |
| `bnb-eth_gettransactionbyblocknumberandindex` | eth_getTransactionByBlockNumberAndIndex | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_gettransactionbyblocknumberandindex.md) |
| `bnb-eth_gettransactionbyhash` | eth_getTransactionByHash | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_gettransactionbyhash.md) |
| `bnb-eth_gettransactioncount` | eth_getTransactionCount | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_gettransactioncount.md) |
| `bnb-eth_gettransactionreceipt` | eth_getTransactionReceipt | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_gettransactionreceipt.md) |
| `bnb-eth_getunclebyblockhashandindex` | eth_getUncleByBlockHashAndIndex | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getunclebyblockhashandindex.md) |
| `bnb-eth_getunclebyblocknumberandindex` | eth_getUncleByBlockNumberAndIndex | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getunclebyblocknumberandindex.md) |
| `bnb-eth_getunclecountbyblockhash` | eth_getUncleCountByBlockHash | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getunclecountbyblockhash.md) |
| `bnb-eth_getunclecountbyblocknumber` | eth_getUncleCountByBlockNumber | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_getunclecountbyblocknumber.md) |
| `bnb-eth_maxpriorityfeepergas` | eth_maxPriorityFeePerGas | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_maxpriorityfeepergas.md) |
| `bnb-eth_newblockfilter` | eth_newBlockFilter | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_newblockfilter.md) |
| `bnb-eth_newfilter` | eth_newFilter | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_newfilter.md) |
| `bnb-eth_newpendingtransactionfilter` | eth_newPendingTransactionFilter | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_newpendingtransactionfilter.md) |
| `bnb-eth_sendrawtransaction` | eth_sendRawTransaction | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_sendrawtransaction.md) |
| `bnb-eth_uninstallfilter` | eth_uninstallFilter | Bnb (mainnet, testnet) | [spec](spec/bnb-eth_uninstallfilter.md) |
| `bnb-net_listening` | net_listening | Bnb (mainnet, testnet) | [spec](spec/bnb-net_listening.md) |
| `bnb-net_version` | net_version | Bnb (mainnet, testnet) | [spec](spec/bnb-net_version.md) |
| `bnb-web3_clientversion` | web3_clientVersion | Bnb (mainnet, testnet) | [spec](spec/bnb-web3_clientversion.md) |
| `bnb-web3_sha3` | web3_sha3 | Bnb (mainnet, testnet) | [spec](spec/bnb-web3_sha3.md) |

## Node API - Bnb Debug (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `bnb-debug_traceblockbyhash` | debug_traceBlockByHash | Bnb (mainnet, testnet) | [spec](spec/bnb-debug_traceblockbyhash.md) |
| `bnb-debug_traceblockbynumber` | debug_traceBlockByNumber | Bnb (mainnet, testnet) | [spec](spec/bnb-debug_traceblockbynumber.md) |
| `bnb-debug_tracecall` | debug_traceCall | Bnb (mainnet, testnet) | [spec](spec/bnb-debug_tracecall.md) |
| `bnb-debug_tracetransaction` | debug_traceTransaction | Bnb (mainnet, testnet) | [spec](spec/bnb-debug_tracetransaction.md) |

## Node API - Ethereum (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `ethereum-eth_blocknumber` | eth_blockNumber | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_blocknumber.md) |
| `ethereum-eth_call` | eth_call | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_call.md) |
| `ethereum-eth_chainid` | eth_chainId | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_chainid.md) |
| `ethereum-eth_createaccesslist` | eth_createAccessList | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_createaccesslist.md) |
| `ethereum-eth_estimategas` | eth_estimateGas | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_estimategas.md) |
| `ethereum-eth_feehistory` | eth_feeHistory | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_feehistory.md) |
| `ethereum-eth_gasprice` | eth_gasPrice | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_gasprice.md) |
| `ethereum-eth_getbalance` | eth_getBalance | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getbalance.md) |
| `ethereum-eth_getblockbyhash` | eth_getBlockByHash | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getblockbyhash.md) |
| `ethereum-eth_getblockbynumber` | eth_getBlockByNumber | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getblockbynumber.md) |
| `ethereum-eth_getblockreceipts` | eth_getBlockReceipts | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getblockreceipts.md) |
| `ethereum-eth_getblocktransactioncountbyhash` | eth_getBlockTransactionCountByHash | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getblocktransactioncountbyhash.md) |
| `ethereum-eth_getblocktransactioncountbynumber` | eth_getBlockTransactionCountByNumber | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getblocktransactioncountbynumber.md) |
| `ethereum-eth_getcode` | eth_getCode | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getcode.md) |
| `ethereum-eth_getfilterchanges` | eth_getFilterChanges | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getfilterchanges.md) |
| `ethereum-eth_getfilterlogs` | eth_getFilterLogs | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getfilterlogs.md) |
| `ethereum-eth_getlogs` | eth_getLogs | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getlogs.md) |
| `ethereum-eth_getproof` | eth_getProof | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getproof.md) |
| `ethereum-eth_getstorageat` | eth_getStorageAt | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getstorageat.md) |
| `ethereum-eth_gettransactionbyblockhashandindex` | eth_getTransactionByBlockHashAndIndex | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_gettransactionbyblockhashandindex.md) |
| `ethereum-eth_gettransactionbyblocknumberandindex` | eth_getTransactionByBlockNumberAndIndex | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_gettransactionbyblocknumberandindex.md) |
| `ethereum-eth_gettransactionbyhash` | eth_getTransactionByHash | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_gettransactionbyhash.md) |
| `ethereum-eth_gettransactioncount` | eth_getTransactionCount | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_gettransactioncount.md) |
| `ethereum-eth_gettransactionreceipt` | eth_getTransactionReceipt | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_gettransactionreceipt.md) |
| `ethereum-eth_getunclebyblockhashandindex` | eth_getUncleByBlockHashAndIndex | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getunclebyblockhashandindex.md) |
| `ethereum-eth_getunclebyblocknumberandindex` | eth_getUncleByBlockNumberAndIndex | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getunclebyblocknumberandindex.md) |
| `ethereum-eth_getunclecountbyblockhash` | eth_getUncleCountByBlockHash | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getunclecountbyblockhash.md) |
| `ethereum-eth_getunclecountbyblocknumber` | eth_getUncleCountByBlockNumber | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_getunclecountbyblocknumber.md) |
| `ethereum-eth_maxpriorityfeepergas` | eth_maxPriorityFeePerGas | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_maxpriorityfeepergas.md) |
| `ethereum-eth_newblockfilter` | eth_newBlockFilter | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_newblockfilter.md) |
| `ethereum-eth_newfilter` | eth_newFilter | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_newfilter.md) |
| `ethereum-eth_newpendingtransactionfilter` | eth_newPendingTransactionFilter | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_newpendingtransactionfilter.md) |
| `ethereum-eth_sendrawtransaction` | eth_sendRawTransaction | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_sendrawtransaction.md) |
| `ethereum-eth_uninstallfilter` | eth_uninstallFilter | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-eth_uninstallfilter.md) |
| `ethereum-net_listening` | net_listening | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-net_listening.md) |
| `ethereum-net_version` | net_version | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-net_version.md) |
| `ethereum-trace_block` | trace_block | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-trace_block.md) |
| `ethereum-trace_call` | trace_call | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-trace_call.md) |
| `ethereum-trace_filter` | trace_filter | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-trace_filter.md) |
| `ethereum-trace_get` | trace_get | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-trace_get.md) |
| `ethereum-trace_replayblocktransactions` | trace_replayBlockTransactions | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-trace_replayblocktransactions.md) |
| `ethereum-trace_replaytransaction` | trace_replayTransaction | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-trace_replaytransaction.md) |
| `ethereum-trace_transaction` | trace_transaction | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-trace_transaction.md) |
| `ethereum-web3_clientversion` | web3_clientVersion | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-web3_clientversion.md) |
| `ethereum-web3_sha3` | web3_sha3 | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-web3_sha3.md) |

## Node API - Ethereum Debug (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `ethereum-debug_traceblockbyhash` | debug_traceBlockByHash | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-debug_traceblockbyhash.md) |
| `ethereum-debug_traceblockbynumber` | debug_traceBlockByNumber | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-debug_traceblockbynumber.md) |
| `ethereum-debug_tracecall` | debug_traceCall | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-debug_tracecall.md) |
| `ethereum-debug_tracetransaction` | debug_traceTransaction | Ethereum (mainnet, sepolia, hoodi) | [spec](spec/ethereum-debug_tracetransaction.md) |

## Node API - Giwa (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `giwa-eth_blocknumber` | eth_blockNumber | Giwa (sepolia) | [spec](spec/giwa-eth_blocknumber.md) |
| `giwa-eth_call` | eth_call | Giwa (sepolia) | [spec](spec/giwa-eth_call.md) |
| `giwa-eth_chainid` | eth_chainId | Giwa (sepolia) | [spec](spec/giwa-eth_chainid.md) |
| `giwa-eth_createaccesslist` | eth_createAccessList | Giwa (sepolia) | [spec](spec/giwa-eth_createaccesslist.md) |
| `giwa-eth_estimategas` | eth_estimateGas | Giwa (sepolia) | [spec](spec/giwa-eth_estimategas.md) |
| `giwa-eth_feehistory` | eth_feeHistory | Giwa (sepolia) | [spec](spec/giwa-eth_feehistory.md) |
| `giwa-eth_gasprice` | eth_gasPrice | Giwa (sepolia) | [spec](spec/giwa-eth_gasprice.md) |
| `giwa-eth_getbalance` | eth_getBalance | Giwa (sepolia) | [spec](spec/giwa-eth_getbalance.md) |
| `giwa-eth_getblockbyhash` | eth_getBlockByHash | Giwa (sepolia) | [spec](spec/giwa-eth_getblockbyhash.md) |
| `giwa-eth_getblockbynumber` | eth_getBlockByNumber | Giwa (sepolia) | [spec](spec/giwa-eth_getblockbynumber.md) |
| `giwa-eth_getblockreceipts` | eth_getBlockReceipts | Giwa (sepolia) | [spec](spec/giwa-eth_getblockreceipts.md) |
| `giwa-eth_getblocktransactioncountbyhash` | eth_getBlockTransactionCountByHash | Giwa (sepolia) | [spec](spec/giwa-eth_getblocktransactioncountbyhash.md) |
| `giwa-eth_getblocktransactioncountbynumber` | eth_getBlockTransactionCountByNumber | Giwa (sepolia) | [spec](spec/giwa-eth_getblocktransactioncountbynumber.md) |
| `giwa-eth_getcode` | eth_getCode | Giwa (sepolia) | [spec](spec/giwa-eth_getcode.md) |
| `giwa-eth_getfilterchanges` | eth_getFilterChanges | Giwa (sepolia) | [spec](spec/giwa-eth_getfilterchanges.md) |
| `giwa-eth_getfilterlogs` | eth_getFilterLogs | Giwa (sepolia) | [spec](spec/giwa-eth_getfilterlogs.md) |
| `giwa-eth_getlogs` | eth_getLogs | Giwa (sepolia) | [spec](spec/giwa-eth_getlogs.md) |
| `giwa-eth_getproof` | eth_getProof | Giwa (sepolia) | [spec](spec/giwa-eth_getproof.md) |
| `giwa-eth_getstorageat` | eth_getStorageAt | Giwa (sepolia) | [spec](spec/giwa-eth_getstorageat.md) |
| `giwa-eth_gettransactionbyblockhashandindex` | eth_getTransactionByBlockHashAndIndex | Giwa (sepolia) | [spec](spec/giwa-eth_gettransactionbyblockhashandindex.md) |
| `giwa-eth_gettransactionbyblocknumberandindex` | eth_getTransactionByBlockNumberAndIndex | Giwa (sepolia) | [spec](spec/giwa-eth_gettransactionbyblocknumberandindex.md) |
| `giwa-eth_gettransactionbyhash` | eth_getTransactionByHash | Giwa (sepolia) | [spec](spec/giwa-eth_gettransactionbyhash.md) |
| `giwa-eth_gettransactioncount` | eth_getTransactionCount | Giwa (sepolia) | [spec](spec/giwa-eth_gettransactioncount.md) |
| `giwa-eth_gettransactionreceipt` | eth_getTransactionReceipt | Giwa (sepolia) | [spec](spec/giwa-eth_gettransactionreceipt.md) |
| `giwa-eth_getunclebyblockhashandindex` | eth_getUncleByBlockHashAndIndex | Giwa (sepolia) | [spec](spec/giwa-eth_getunclebyblockhashandindex.md) |
| `giwa-eth_getunclebyblocknumberandindex` | eth_getUncleByBlockNumberAndIndex | Giwa (sepolia) | [spec](spec/giwa-eth_getunclebyblocknumberandindex.md) |
| `giwa-eth_getunclecountbyblockhash` | eth_getUncleCountByBlockHash | Giwa (sepolia) | [spec](spec/giwa-eth_getunclecountbyblockhash.md) |
| `giwa-eth_getunclecountbyblocknumber` | eth_getUncleCountByBlockNumber | Giwa (sepolia) | [spec](spec/giwa-eth_getunclecountbyblocknumber.md) |
| `giwa-eth_maxpriorityfeepergas` | eth_maxPriorityFeePerGas | Giwa (sepolia) | [spec](spec/giwa-eth_maxpriorityfeepergas.md) |
| `giwa-eth_newblockfilter` | eth_newBlockFilter | Giwa (sepolia) | [spec](spec/giwa-eth_newblockfilter.md) |
| `giwa-eth_newfilter` | eth_newFilter | Giwa (sepolia) | [spec](spec/giwa-eth_newfilter.md) |
| `giwa-eth_newpendingtransactionfilter` | eth_newPendingTransactionFilter | Giwa (sepolia) | [spec](spec/giwa-eth_newpendingtransactionfilter.md) |
| `giwa-eth_sendrawtransaction` | eth_sendRawTransaction | Giwa (sepolia) | [spec](spec/giwa-eth_sendrawtransaction.md) |
| `giwa-eth_uninstallfilter` | eth_uninstallFilter | Giwa (sepolia) | [spec](spec/giwa-eth_uninstallfilter.md) |
| `giwa-net_listening` | net_listening | Giwa (sepolia) | [spec](spec/giwa-net_listening.md) |
| `giwa-net_version` | net_version | Giwa (sepolia) | [spec](spec/giwa-net_version.md) |
| `giwa-optimism_outputatblock` | optimism_outputAtBlock | Giwa (sepolia) | [spec](spec/giwa-optimism_outputatblock.md) |
| `giwa-optimism_rollupconfig` | optimism_rollupConfig | Giwa (sepolia) | [spec](spec/giwa-optimism_rollupconfig.md) |
| `giwa-web3_clientversion` | web3_clientVersion | Giwa (sepolia) | [spec](spec/giwa-web3_clientversion.md) |
| `giwa-web3_sha3` | web3_sha3 | Giwa (sepolia) | [spec](spec/giwa-web3_sha3.md) |

## Node API - Giwa Debug (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `giwa-debug_traceblockbyhash` | debug_traceBlockByHash | Giwa (sepolia) | [spec](spec/giwa-debug_traceblockbyhash.md) |
| `giwa-debug_traceblockbynumber` | debug_traceBlockByNumber | Giwa (sepolia) | [spec](spec/giwa-debug_traceblockbynumber.md) |
| `giwa-debug_tracecall` | debug_traceCall | Giwa (sepolia) | [spec](spec/giwa-debug_tracecall.md) |
| `giwa-debug_tracetransaction` | debug_traceTransaction | Giwa (sepolia) | [spec](spec/giwa-debug_tracetransaction.md) |

## Node API - Kaia (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `kaia-eth_blocknumber` | eth_blockNumber | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_blocknumber.md) |
| `kaia-eth_call` | eth_call | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_call.md) |
| `kaia-eth_chainid` | eth_chainId | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_chainid.md) |
| `kaia-eth_createaccesslist` | eth_createAccessList | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_createaccesslist.md) |
| `kaia-eth_estimategas` | eth_estimateGas | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_estimategas.md) |
| `kaia-eth_feehistory` | eth_feeHistory | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_feehistory.md) |
| `kaia-eth_gasprice` | eth_gasPrice | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_gasprice.md) |
| `kaia-eth_getbalance` | eth_getBalance | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getbalance.md) |
| `kaia-eth_getblockbyhash` | eth_getBlockByHash | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getblockbyhash.md) |
| `kaia-eth_getblockbynumber` | eth_getBlockByNumber | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getblockbynumber.md) |
| `kaia-eth_getblockreceipts` | eth_getBlockReceipts | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getblockreceipts.md) |
| `kaia-eth_getblocktransactioncountbyhash` | eth_getBlockTransactionCountByHash | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getblocktransactioncountbyhash.md) |
| `kaia-eth_getblocktransactioncountbynumber` | eth_getBlockTransactionCountByNumber | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getblocktransactioncountbynumber.md) |
| `kaia-eth_getcode` | eth_getCode | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getcode.md) |
| `kaia-eth_getfilterchanges` | eth_getFilterChanges | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getfilterchanges.md) |
| `kaia-eth_getfilterlogs` | eth_getFilterLogs | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getfilterlogs.md) |
| `kaia-eth_getlogs` | eth_getLogs | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getlogs.md) |
| `kaia-eth_getproof` | eth_getProof | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getproof.md) |
| `kaia-eth_getstorageat` | eth_getStorageAt | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getstorageat.md) |
| `kaia-eth_gettransactionbyblockhashandindex` | eth_getTransactionByBlockHashAndIndex | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_gettransactionbyblockhashandindex.md) |
| `kaia-eth_gettransactionbyblocknumberandindex` | eth_getTransactionByBlockNumberAndIndex | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_gettransactionbyblocknumberandindex.md) |
| `kaia-eth_gettransactionbyhash` | eth_getTransactionByHash | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_gettransactionbyhash.md) |
| `kaia-eth_gettransactioncount` | eth_getTransactionCount | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_gettransactioncount.md) |
| `kaia-eth_gettransactionreceipt` | eth_getTransactionReceipt | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_gettransactionreceipt.md) |
| `kaia-eth_getunclebyblockhashandindex` | eth_getUncleByBlockHashAndIndex | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getunclebyblockhashandindex.md) |
| `kaia-eth_getunclebyblocknumberandindex` | eth_getUncleByBlockNumberAndIndex | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getunclebyblocknumberandindex.md) |
| `kaia-eth_getunclecountbyblockhash` | eth_getUncleCountByBlockHash | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getunclecountbyblockhash.md) |
| `kaia-eth_getunclecountbyblocknumber` | eth_getUncleCountByBlockNumber | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_getunclecountbyblocknumber.md) |
| `kaia-eth_maxpriorityfeepergas` | eth_maxPriorityFeePerGas | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_maxpriorityfeepergas.md) |
| `kaia-eth_newblockfilter` | eth_newBlockFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_newblockfilter.md) |
| `kaia-eth_newfilter` | eth_newFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_newfilter.md) |
| `kaia-eth_newpendingtransactionfilter` | eth_newPendingTransactionFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_newpendingtransactionfilter.md) |
| `kaia-eth_sendrawtransaction` | eth_sendRawTransaction | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_sendrawtransaction.md) |
| `kaia-eth_uninstallfilter` | eth_uninstallFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-eth_uninstallfilter.md) |
| `kaia-kaia_blocknumber` | kaia_blockNumber | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_blocknumber.md) |
| `kaia-kaia_call` | kaia_call | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_call.md) |
| `kaia-kaia_chainid` | kaia_chainID | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_chainid.md) |
| `kaia-kaia_createaccesslist` | kaia_createAccessList | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_createaccesslist.md) |
| `kaia-kaia_estimategas` | kaia_estimateGas | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_estimategas.md) |
| `kaia-kaia_feehistory` | kaia_feeHistory | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_feehistory.md) |
| `kaia-kaia_gasprice` | kaia_gasPrice | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_gasprice.md) |
| `kaia-kaia_getbalance` | kaia_getBalance | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getbalance.md) |
| `kaia-kaia_getblockbyhash` | kaia_getBlockByHash | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getblockbyhash.md) |
| `kaia-kaia_getblockbynumber` | kaia_getBlockByNumber | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getblockbynumber.md) |
| `kaia-kaia_getblockreceipts` | kaia_getBlockReceipts | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getblockreceipts.md) |
| `kaia-kaia_getblocktransactioncountbyhash` | kaia_getBlockTransactionCountByHash | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getblocktransactioncountbyhash.md) |
| `kaia-kaia_getblocktransactioncountbynumber` | kaia_getBlockTransactionCountByNumber | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getblocktransactioncountbynumber.md) |
| `kaia-kaia_getcode` | kaia_getCode | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getcode.md) |
| `kaia-kaia_getfilterchanges` | kaia_getFilterChanges | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getfilterchanges.md) |
| `kaia-kaia_getfilterlogs` | kaia_getFilterLogs | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getfilterlogs.md) |
| `kaia-kaia_getlogs` | kaia_getLogs | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getlogs.md) |
| `kaia-kaia_getproof` | kaia_getProof | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getproof.md) |
| `kaia-kaia_getrewards` | kaia_getRewards | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getrewards.md) |
| `kaia-kaia_getstorageat` | kaia_getStorageAt | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_getstorageat.md) |
| `kaia-kaia_gettransactionbyblockhashandindex` | kaia_getTransactionByBlockHashAndIndex | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_gettransactionbyblockhashandindex.md) |
| `kaia-kaia_gettransactionbyblocknumberandindex` | kaia_getTransactionByBlockNumberAndIndex | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_gettransactionbyblocknumberandindex.md) |
| `kaia-kaia_gettransactionbyhash` | kaia_getTransactionByHash | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_gettransactionbyhash.md) |
| `kaia-kaia_gettransactioncount` | kaia_getTransactionCount | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_gettransactioncount.md) |
| `kaia-kaia_gettransactionreceipt` | kaia_getTransactionReceipt | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_gettransactionreceipt.md) |
| `kaia-kaia_maxpriorityfeepergas` | kaia_maxPriorityFeePerGas | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_maxpriorityfeepergas.md) |
| `kaia-kaia_newblockfilter` | kaia_newBlockFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_newblockfilter.md) |
| `kaia-kaia_newfilter` | kaia_newFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_newfilter.md) |
| `kaia-kaia_newpendingtransactionfilter` | kaia_newPendingTransactionFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_newpendingtransactionfilter.md) |
| `kaia-kaia_sendrawtransaction` | kaia_sendRawTransaction | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_sendrawtransaction.md) |
| `kaia-kaia_uninstallfilter` | kaia_uninstallFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-kaia_uninstallfilter.md) |
| `kaia-klay_blocknumber` | klay_blockNumber | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_blocknumber.md) |
| `kaia-klay_call` | klay_call | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_call.md) |
| `kaia-klay_chainid` | klay_chainID | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_chainid.md) |
| `kaia-klay_createaccesslist` | klay_createAccessList | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_createaccesslist.md) |
| `kaia-klay_estimategas` | klay_estimateGas | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_estimategas.md) |
| `kaia-klay_feehistory` | klay_feeHistory | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_feehistory.md) |
| `kaia-klay_gasprice` | klay_gasPrice | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_gasprice.md) |
| `kaia-klay_getbalance` | klay_getBalance | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getbalance.md) |
| `kaia-klay_getblockbyhash` | klay_getBlockByHash | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getblockbyhash.md) |
| `kaia-klay_getblockbynumber` | klay_getBlockByNumber | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getblockbynumber.md) |
| `kaia-klay_getblockreceipts` | klay_getBlockReceipts | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getblockreceipts.md) |
| `kaia-klay_getblocktransactioncountbyhash` | klay_getBlockTransactionCountByHash | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getblocktransactioncountbyhash.md) |
| `kaia-klay_getblocktransactioncountbynumber` | klay_getBlockTransactionCountByNumber | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getblocktransactioncountbynumber.md) |
| `kaia-klay_getcode` | klay_getCode | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getcode.md) |
| `kaia-klay_getfilterchanges` | klay_getFilterChanges | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getfilterchanges.md) |
| `kaia-klay_getfilterlogs` | klay_getFilterLogs | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getfilterlogs.md) |
| `kaia-klay_getlogs` | klay_getLogs | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getlogs.md) |
| `kaia-klay_getproof` | klay_getProof | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getproof.md) |
| `kaia-klay_getstorageat` | klay_getStorageAt | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_getstorageat.md) |
| `kaia-klay_gettransactionbyblockhashandindex` | klay_getTransactionByBlockHashAndIndex | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_gettransactionbyblockhashandindex.md) |
| `kaia-klay_gettransactionbyblocknumberandindex` | klay_getTransactionByBlockNumberAndIndex | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_gettransactionbyblocknumberandindex.md) |
| `kaia-klay_gettransactionbyhash` | klay_getTransactionByHash | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_gettransactionbyhash.md) |
| `kaia-klay_gettransactioncount` | klay_getTransactionCount | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_gettransactioncount.md) |
| `kaia-klay_gettransactionreceipt` | klay_getTransactionReceipt | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_gettransactionreceipt.md) |
| `kaia-klay_maxpriorityfeepergas` | klay_maxPriorityFeePerGas | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_maxpriorityfeepergas.md) |
| `kaia-klay_newblockfilter` | klay_newBlockFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_newblockfilter.md) |
| `kaia-klay_newfilter` | klay_newFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_newfilter.md) |
| `kaia-klay_newpendingtransactionfilter` | klay_newPendingTransactionFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_newpendingtransactionfilter.md) |
| `kaia-klay_sendrawtransaction` | klay_sendRawTransaction | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_sendrawtransaction.md) |
| `kaia-klay_uninstallfilter` | klay_uninstallFilter | Kaia (mainnet, kairos) | [spec](spec/kaia-klay_uninstallfilter.md) |
| `kaia-net_listening` | net_listening | Kaia (mainnet, kairos) | [spec](spec/kaia-net_listening.md) |
| `kaia-net_version` | net_version | Kaia (mainnet, kairos) | [spec](spec/kaia-net_version.md) |
| `kaia-web3_clientversion` | web3_clientVersion | Kaia (mainnet, kairos) | [spec](spec/kaia-web3_clientversion.md) |
| `kaia-web3_sha3` | web3_sha3 | Kaia (mainnet, kairos) | [spec](spec/kaia-web3_sha3.md) |

## Node API - Kaia Debug (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `kaia-debug_traceblockbyhash` | debug_traceBlockByHash | Kaia (mainnet, kairos) | [spec](spec/kaia-debug_traceblockbyhash.md) |
| `kaia-debug_traceblockbynumber` | debug_traceBlockByNumber | Kaia (mainnet, kairos) | [spec](spec/kaia-debug_traceblockbynumber.md) |
| `kaia-debug_tracecall` | debug_traceCall | Kaia (mainnet, kairos) | [spec](spec/kaia-debug_tracecall.md) |
| `kaia-debug_tracetransaction` | debug_traceTransaction | Kaia (mainnet, kairos) | [spec](spec/kaia-debug_tracetransaction.md) |

## Node API - Luniverse (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `luniverse-eth_blocknumber` | eth_blockNumber | Luniverse (mainnet) | [spec](spec/luniverse-eth_blocknumber.md) |
| `luniverse-eth_call` | eth_call | Luniverse (mainnet) | [spec](spec/luniverse-eth_call.md) |
| `luniverse-eth_chainid` | eth_chainId | Luniverse (mainnet) | [spec](spec/luniverse-eth_chainid.md) |
| `luniverse-eth_createaccesslist` | eth_createAccessList | Luniverse (mainnet) | [spec](spec/luniverse-eth_createaccesslist.md) |
| `luniverse-eth_estimategas` | eth_estimateGas | Luniverse (mainnet) | [spec](spec/luniverse-eth_estimategas.md) |
| `luniverse-eth_feehistory` | eth_feeHistory | Luniverse (mainnet) | [spec](spec/luniverse-eth_feehistory.md) |
| `luniverse-eth_gasprice` | eth_gasPrice | Luniverse (mainnet) | [spec](spec/luniverse-eth_gasprice.md) |
| `luniverse-eth_getbalance` | eth_getBalance | Luniverse (mainnet) | [spec](spec/luniverse-eth_getbalance.md) |
| `luniverse-eth_getblockbyhash` | eth_getBlockByHash | Luniverse (mainnet) | [spec](spec/luniverse-eth_getblockbyhash.md) |
| `luniverse-eth_getblockbynumber` | eth_getBlockByNumber | Luniverse (mainnet) | [spec](spec/luniverse-eth_getblockbynumber.md) |
| `luniverse-eth_getblocktransactioncountbyhash` | eth_getBlockTransactionCountByHash | Luniverse (mainnet) | [spec](spec/luniverse-eth_getblocktransactioncountbyhash.md) |
| `luniverse-eth_getblocktransactioncountbynumber` | eth_getBlockTransactionCountByNumber | Luniverse (mainnet) | [spec](spec/luniverse-eth_getblocktransactioncountbynumber.md) |
| `luniverse-eth_getcode` | eth_getCode | Luniverse (mainnet) | [spec](spec/luniverse-eth_getcode.md) |
| `luniverse-eth_getfilterchanges` | eth_getFilterChanges | Luniverse (mainnet) | [spec](spec/luniverse-eth_getfilterchanges.md) |
| `luniverse-eth_getfilterlogs` | eth_getFilterLogs | Luniverse (mainnet) | [spec](spec/luniverse-eth_getfilterlogs.md) |
| `luniverse-eth_getlogs` | eth_getLogs | Luniverse (mainnet) | [spec](spec/luniverse-eth_getlogs.md) |
| `luniverse-eth_getproof` | eth_getProof | Luniverse (mainnet) | [spec](spec/luniverse-eth_getproof.md) |
| `luniverse-eth_getstorageat` | eth_getStorageAt | Luniverse (mainnet) | [spec](spec/luniverse-eth_getstorageat.md) |
| `luniverse-eth_gettransactionbyblockhashandindex` | eth_getTransactionByBlockHashAndIndex | Luniverse (mainnet) | [spec](spec/luniverse-eth_gettransactionbyblockhashandindex.md) |
| `luniverse-eth_gettransactionbyblocknumberandindex` | eth_getTransactionByBlockNumberAndIndex | Luniverse (mainnet) | [spec](spec/luniverse-eth_gettransactionbyblocknumberandindex.md) |
| `luniverse-eth_gettransactionbyhash` | eth_getTransactionByHash | Luniverse (mainnet) | [spec](spec/luniverse-eth_gettransactionbyhash.md) |
| `luniverse-eth_gettransactioncount` | eth_getTransactionCount | Luniverse (mainnet) | [spec](spec/luniverse-eth_gettransactioncount.md) |
| `luniverse-eth_gettransactionreceipt` | eth_getTransactionReceipt | Luniverse (mainnet) | [spec](spec/luniverse-eth_gettransactionreceipt.md) |
| `luniverse-eth_getunclebyblockhashandindex` | eth_getUncleByBlockHashAndIndex | Luniverse (mainnet) | [spec](spec/luniverse-eth_getunclebyblockhashandindex.md) |
| `luniverse-eth_getunclebyblocknumberandindex` | eth_getUncleByBlockNumberAndIndex | Luniverse (mainnet) | [spec](spec/luniverse-eth_getunclebyblocknumberandindex.md) |
| `luniverse-eth_getunclecountbyblockhash` | eth_getUncleCountByBlockHash | Luniverse (mainnet) | [spec](spec/luniverse-eth_getunclecountbyblockhash.md) |
| `luniverse-eth_getunclecountbyblocknumber` | eth_getUncleCountByBlockNumber | Luniverse (mainnet) | [spec](spec/luniverse-eth_getunclecountbyblocknumber.md) |
| `luniverse-eth_maxpriorityfeepergas` | eth_maxPriorityFeePerGas | Luniverse (mainnet) | [spec](spec/luniverse-eth_maxpriorityfeepergas.md) |
| `luniverse-eth_newblockfilter` | eth_newBlockFilter | Luniverse (mainnet) | [spec](spec/luniverse-eth_newblockfilter.md) |
| `luniverse-eth_newfilter` | eth_newFilter | Luniverse (mainnet) | [spec](spec/luniverse-eth_newfilter.md) |
| `luniverse-eth_newpendingtransactionfilter` | eth_newPendingTransactionFilter | Luniverse (mainnet) | [spec](spec/luniverse-eth_newpendingtransactionfilter.md) |
| `luniverse-eth_sendrawtransaction` | eth_sendRawTransaction | Luniverse (mainnet) | [spec](spec/luniverse-eth_sendrawtransaction.md) |
| `luniverse-eth_uninstallfilter` | eth_uninstallFilter | Luniverse (mainnet) | [spec](spec/luniverse-eth_uninstallfilter.md) |
| `luniverse-net_listening` | net_listening | Luniverse (mainnet) | [spec](spec/luniverse-net_listening.md) |
| `luniverse-net_version` | net_version | Luniverse (mainnet) | [spec](spec/luniverse-net_version.md) |
| `luniverse-web3_clientversion` | web3_clientVersion | Luniverse (mainnet) | [spec](spec/luniverse-web3_clientversion.md) |
| `luniverse-web3_sha3` | web3_sha3 | Luniverse (mainnet) | [spec](spec/luniverse-web3_sha3.md) |

## Node API - Luniverse Debug (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `luniverse-debug_traceblockbyhash` | debug_traceBlockByHash | Luniverse (mainnet) | [spec](spec/luniverse-debug_traceblockbyhash.md) |
| `luniverse-debug_traceblockbynumber` | debug_traceBlockByNumber | Luniverse (mainnet) | [spec](spec/luniverse-debug_traceblockbynumber.md) |
| `luniverse-debug_tracecall` | debug_traceCall | Luniverse (mainnet) | [spec](spec/luniverse-debug_tracecall.md) |
| `luniverse-debug_tracetransaction` | debug_traceTransaction | Luniverse (mainnet) | [spec](spec/luniverse-debug_tracetransaction.md) |

## Node API - Optimism (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `optimism-eth_blocknumber` | eth_blockNumber | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_blocknumber.md) |
| `optimism-eth_call` | eth_call | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_call.md) |
| `optimism-eth_chainid` | eth_chainId | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_chainid.md) |
| `optimism-eth_createaccesslist` | eth_createAccessList | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_createaccesslist.md) |
| `optimism-eth_estimategas` | eth_estimateGas | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_estimategas.md) |
| `optimism-eth_feehistory` | eth_feeHistory | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_feehistory.md) |
| `optimism-eth_gasprice` | eth_gasPrice | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_gasprice.md) |
| `optimism-eth_getbalance` | eth_getBalance | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getbalance.md) |
| `optimism-eth_getblockbyhash` | eth_getBlockByHash | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getblockbyhash.md) |
| `optimism-eth_getblockbynumber` | eth_getBlockByNumber | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getblockbynumber.md) |
| `optimism-eth_getblockreceipts` | eth_getBlockReceipts | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getblockreceipts.md) |
| `optimism-eth_getblocktransactioncountbyhash` | eth_getBlockTransactionCountByHash | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getblocktransactioncountbyhash.md) |
| `optimism-eth_getblocktransactioncountbynumber` | eth_getBlockTransactionCountByNumber | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getblocktransactioncountbynumber.md) |
| `optimism-eth_getcode` | eth_getCode | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getcode.md) |
| `optimism-eth_getfilterchanges` | eth_getFilterChanges | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getfilterchanges.md) |
| `optimism-eth_getfilterlogs` | eth_getFilterLogs | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getfilterlogs.md) |
| `optimism-eth_getlogs` | eth_getLogs | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getlogs.md) |
| `optimism-eth_getproof` | eth_getProof | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getproof.md) |
| `optimism-eth_getstorageat` | eth_getStorageAt | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getstorageat.md) |
| `optimism-eth_gettransactionbyblockhashandindex` | eth_getTransactionByBlockHashAndIndex | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_gettransactionbyblockhashandindex.md) |
| `optimism-eth_gettransactionbyblocknumberandindex` | eth_getTransactionByBlockNumberAndIndex | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_gettransactionbyblocknumberandindex.md) |
| `optimism-eth_gettransactionbyhash` | eth_getTransactionByHash | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_gettransactionbyhash.md) |
| `optimism-eth_gettransactioncount` | eth_getTransactionCount | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_gettransactioncount.md) |
| `optimism-eth_gettransactionreceipt` | eth_getTransactionReceipt | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_gettransactionreceipt.md) |
| `optimism-eth_getunclebyblockhashandindex` | eth_getUncleByBlockHashAndIndex | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getunclebyblockhashandindex.md) |
| `optimism-eth_getunclebyblocknumberandindex` | eth_getUncleByBlockNumberAndIndex | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getunclebyblocknumberandindex.md) |
| `optimism-eth_getunclecountbyblockhash` | eth_getUncleCountByBlockHash | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getunclecountbyblockhash.md) |
| `optimism-eth_getunclecountbyblocknumber` | eth_getUncleCountByBlockNumber | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_getunclecountbyblocknumber.md) |
| `optimism-eth_maxpriorityfeepergas` | eth_maxPriorityFeePerGas | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_maxpriorityfeepergas.md) |
| `optimism-eth_newblockfilter` | eth_newBlockFilter | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_newblockfilter.md) |
| `optimism-eth_newfilter` | eth_newFilter | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_newfilter.md) |
| `optimism-eth_newpendingtransactionfilter` | eth_newPendingTransactionFilter | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_newpendingtransactionfilter.md) |
| `optimism-eth_sendrawtransaction` | eth_sendRawTransaction | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_sendrawtransaction.md) |
| `optimism-eth_uninstallfilter` | eth_uninstallFilter | Optimism (mainnet, sepolia) | [spec](spec/optimism-eth_uninstallfilter.md) |
| `optimism-net_listening` | net_listening | Optimism (mainnet, sepolia) | [spec](spec/optimism-net_listening.md) |
| `optimism-net_version` | net_version | Optimism (mainnet, sepolia) | [spec](spec/optimism-net_version.md) |
| `optimism-optimism_outputatblock` | optimism_outputAtBlock | Optimism (mainnet, sepolia) | [spec](spec/optimism-optimism_outputatblock.md) |
| `optimism-optimism_rollupconfig` | optimism_rollupConfig | Optimism (mainnet, sepolia) | [spec](spec/optimism-optimism_rollupconfig.md) |
| `optimism-web3_clientversion` | web3_clientVersion | Optimism (mainnet, sepolia) | [spec](spec/optimism-web3_clientversion.md) |
| `optimism-web3_sha3` | web3_sha3 | Optimism (mainnet, sepolia) | [spec](spec/optimism-web3_sha3.md) |

## Node API - Optimism Debug (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `optimism-debug_traceblockbyhash` | debug_traceBlockByHash | Optimism (mainnet, sepolia) | [spec](spec/optimism-debug_traceblockbyhash.md) |
| `optimism-debug_traceblockbynumber` | debug_traceBlockByNumber | Optimism (mainnet, sepolia) | [spec](spec/optimism-debug_traceblockbynumber.md) |
| `optimism-debug_tracecall` | debug_traceCall | Optimism (mainnet, sepolia) | [spec](spec/optimism-debug_tracecall.md) |
| `optimism-debug_tracetransaction` | debug_traceTransaction | Optimism (mainnet, sepolia) | [spec](spec/optimism-debug_tracetransaction.md) |

## Node API - Polygon (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `polygon-eth_blocknumber` | eth_blockNumber | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_blocknumber.md) |
| `polygon-eth_call` | eth_call | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_call.md) |
| `polygon-eth_chainid` | eth_chainId | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_chainid.md) |
| `polygon-eth_createaccesslist` | eth_createAccessList | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_createaccesslist.md) |
| `polygon-eth_estimategas` | eth_estimateGas | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_estimategas.md) |
| `polygon-eth_feehistory` | eth_feeHistory | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_feehistory.md) |
| `polygon-eth_gasprice` | eth_gasPrice | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_gasprice.md) |
| `polygon-eth_getbalance` | eth_getBalance | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getbalance.md) |
| `polygon-eth_getblockbyhash` | eth_getBlockByHash | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getblockbyhash.md) |
| `polygon-eth_getblockbynumber` | eth_getBlockByNumber | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getblockbynumber.md) |
| `polygon-eth_getblocktransactioncountbyhash` | eth_getBlockTransactionCountByHash | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getblocktransactioncountbyhash.md) |
| `polygon-eth_getblocktransactioncountbynumber` | eth_getBlockTransactionCountByNumber | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getblocktransactioncountbynumber.md) |
| `polygon-eth_getcode` | eth_getCode | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getcode.md) |
| `polygon-eth_getfilterchanges` | eth_getFilterChanges | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getfilterchanges.md) |
| `polygon-eth_getfilterlogs` | eth_getFilterLogs | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getfilterlogs.md) |
| `polygon-eth_getlogs` | eth_getLogs | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getlogs.md) |
| `polygon-eth_getproof` | eth_getProof | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getproof.md) |
| `polygon-eth_getstorageat` | eth_getStorageAt | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getstorageat.md) |
| `polygon-eth_gettransactionbyblockhashandindex` | eth_getTransactionByBlockHashAndIndex | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_gettransactionbyblockhashandindex.md) |
| `polygon-eth_gettransactionbyblocknumberandindex` | eth_getTransactionByBlockNumberAndIndex | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_gettransactionbyblocknumberandindex.md) |
| `polygon-eth_gettransactionbyhash` | eth_getTransactionByHash | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_gettransactionbyhash.md) |
| `polygon-eth_gettransactioncount` | eth_getTransactionCount | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_gettransactioncount.md) |
| `polygon-eth_gettransactionreceipt` | eth_getTransactionReceipt | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_gettransactionreceipt.md) |
| `polygon-eth_getunclebyblockhashandindex` | eth_getUncleByBlockHashAndIndex | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getunclebyblockhashandindex.md) |
| `polygon-eth_getunclebyblocknumberandindex` | eth_getUncleByBlockNumberAndIndex | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getunclebyblocknumberandindex.md) |
| `polygon-eth_getunclecountbyblockhash` | eth_getUncleCountByBlockHash | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getunclecountbyblockhash.md) |
| `polygon-eth_getunclecountbyblocknumber` | eth_getUncleCountByBlockNumber | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_getunclecountbyblocknumber.md) |
| `polygon-eth_maxpriorityfeepergas` | eth_maxPriorityFeePerGas | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_maxpriorityfeepergas.md) |
| `polygon-eth_newblockfilter` | eth_newBlockFilter | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_newblockfilter.md) |
| `polygon-eth_newfilter` | eth_newFilter | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_newfilter.md) |
| `polygon-eth_newpendingtransactionfilter` | eth_newPendingTransactionFilter | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_newpendingtransactionfilter.md) |
| `polygon-eth_sendrawtransaction` | eth_sendRawTransaction | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_sendrawtransaction.md) |
| `polygon-eth_uninstallfilter` | eth_uninstallFilter | Polygon (mainnet, amoy) | [spec](spec/polygon-eth_uninstallfilter.md) |
| `polygon-net_listening` | net_listening | Polygon (mainnet, amoy) | [spec](spec/polygon-net_listening.md) |
| `polygon-net_version` | net_version | Polygon (mainnet, amoy) | [spec](spec/polygon-net_version.md) |
| `polygon-web3_clientversion` | web3_clientVersion | Polygon (mainnet, amoy) | [spec](spec/polygon-web3_clientversion.md) |
| `polygon-web3_sha3` | web3_sha3 | Polygon (mainnet, amoy) | [spec](spec/polygon-web3_sha3.md) |

## Node API - Polygon Bor (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `polygon-bor_getauthor` | bor_getAuthor | Polygon (mainnet, amoy) | [spec](spec/polygon-bor_getauthor.md) |
| `polygon-bor_getcurrentproposer` | bor_getCurrentProposer | Polygon (mainnet, amoy) | [spec](spec/polygon-bor_getcurrentproposer.md) |
| `polygon-bor_getcurrentvalidators` | bor_getCurrentValidators | Polygon (mainnet, amoy) | [spec](spec/polygon-bor_getcurrentvalidators.md) |
| `polygon-bor_getsignersathash` | bor_getSignersAtHash | Polygon (mainnet, amoy) | [spec](spec/polygon-bor_getsignersathash.md) |

## Node API - Polygon Debug (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `polygon-debug_traceblockbyhash` | debug_traceBlockByHash | Polygon (mainnet, amoy) | [spec](spec/polygon-debug_traceblockbyhash.md) |
| `polygon-debug_traceblockbynumber` | debug_traceBlockByNumber | Polygon (mainnet, amoy) | [spec](spec/polygon-debug_traceblockbynumber.md) |
| `polygon-debug_tracecall` | debug_traceCall | Polygon (mainnet, amoy) | [spec](spec/polygon-debug_tracecall.md) |
| `polygon-debug_tracetransaction` | debug_traceTransaction | Polygon (mainnet, amoy) | [spec](spec/polygon-debug_tracetransaction.md) |

## Node API - Solana (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `solana-getAccountInfo` | getAccountInfo | Solana (mainnet, devnet) | [spec](spec/solana-getAccountInfo.md) |
| `solana-getBalance` | getBalance | Solana (mainnet, devnet) | [spec](spec/solana-getBalance.md) |
| `solana-getBlock` | getBlock | Solana (mainnet, devnet) | [spec](spec/solana-getBlock.md) |
| `solana-getBlockCommitment` | getBlockCommitment | Solana (mainnet, devnet) | [spec](spec/solana-getBlockCommitment.md) |
| `solana-getBlockHeight` | getBlockHeight | Solana (mainnet, devnet) | [spec](spec/solana-getBlockHeight.md) |
| `solana-getBlockProduction` | getBlockProduction | Solana (mainnet, devnet) | [spec](spec/solana-getBlockProduction.md) |
| `solana-getBlockTime` | getBlockTime | Solana (mainnet, devnet) | [spec](spec/solana-getBlockTime.md) |
| `solana-getBlocks` | getBlocks | Solana (mainnet, devnet) | [spec](spec/solana-getBlocks.md) |
| `solana-getBlocksWithLimit` | getBlocksWithLimit | Solana (mainnet, devnet) | [spec](spec/solana-getBlocksWithLimit.md) |
| `solana-getClusterNodes` | getClusterNodes | Solana (mainnet, devnet) | [spec](spec/solana-getClusterNodes.md) |
| `solana-getEpochInfo` | getEpochInfo | Solana (mainnet, devnet) | [spec](spec/solana-getEpochInfo.md) |
| `solana-getEpochSchedule` | getEpochSchedule | Solana (mainnet, devnet) | [spec](spec/solana-getEpochSchedule.md) |
| `solana-getFeeForMessage` | getFeeForMessage | Solana (mainnet, devnet) | [spec](spec/solana-getFeeForMessage.md) |
| `solana-getFirstAvailableBlock` | getFirstAvailableBlock | Solana (mainnet, devnet) | [spec](spec/solana-getFirstAvailableBlock.md) |
| `solana-getGenesisHash` | getGenesisHash | Solana (mainnet, devnet) | [spec](spec/solana-getGenesisHash.md) |
| `solana-getHealth` | getHealth | Solana (mainnet, devnet) | [spec](spec/solana-getHealth.md) |
| `solana-getHighestSnapshotSlot` | getHighestSnapshotSlot | Solana (mainnet, devnet) | [spec](spec/solana-getHighestSnapshotSlot.md) |
| `solana-getIdentity` | getIdentity | Solana (mainnet, devnet) | [spec](spec/solana-getIdentity.md) |
| `solana-getInflationGovernor` | getInflationGovernor | Solana (mainnet, devnet) | [spec](spec/solana-getInflationGovernor.md) |
| `solana-getInflationRate` | getInflationRate | Solana (mainnet, devnet) | [spec](spec/solana-getInflationRate.md) |
| `solana-getInflationReward` | getInflationReward | Solana (mainnet, devnet) | [spec](spec/solana-getInflationReward.md) |
| `solana-getLatestBlockhash` | getLatestBlockhash | Solana (mainnet, devnet) | [spec](spec/solana-getLatestBlockhash.md) |
| `solana-getLeaderSchedule` | getLeaderSchedule | Solana (mainnet, devnet) | [spec](spec/solana-getLeaderSchedule.md) |
| `solana-getMaxRetransmitSlot` | getMaxRetransmitSlot | Solana (mainnet, devnet) | [spec](spec/solana-getMaxRetransmitSlot.md) |
| `solana-getMaxShredInsertSlot` | getMaxShredInsertSlot | Solana (mainnet, devnet) | [spec](spec/solana-getMaxShredInsertSlot.md) |
| `solana-getMinimumBalanceForRentExemption` | getMinimumBalanceForRentExemption | Solana (mainnet, devnet) | [spec](spec/solana-getMinimumBalanceForRentExemption.md) |
| `solana-getMultipleAccounts` | getMultipleAccounts | Solana (mainnet, devnet) | [spec](spec/solana-getMultipleAccounts.md) |
| `solana-getProgramAccounts` | getProgramAccounts | Solana (mainnet, devnet) | [spec](spec/solana-getProgramAccounts.md) |
| `solana-getRecentPerformanceSamples` | getRecentPerformanceSamples | Solana (mainnet, devnet) | [spec](spec/solana-getRecentPerformanceSamples.md) |
| `solana-getRecentPrioritizationFees` | getRecentPrioritizationFees | Solana (mainnet, devnet) | [spec](spec/solana-getRecentPrioritizationFees.md) |
| `solana-getSignatureStatuses` | getSignatureStatuses | Solana (mainnet, devnet) | [spec](spec/solana-getSignatureStatuses.md) |
| `solana-getSignaturesForAddress` | getSignaturesForAddress | Solana (mainnet, devnet) | [spec](spec/solana-getSignaturesForAddress.md) |
| `solana-getSlot` | getSlot | Solana (mainnet, devnet) | [spec](spec/solana-getSlot.md) |
| `solana-getSlotLeader` | getSlotLeader | Solana (mainnet, devnet) | [spec](spec/solana-getSlotLeader.md) |
| `solana-getSlotLeaders` | getSlotLeaders | Solana (mainnet, devnet) | [spec](spec/solana-getSlotLeaders.md) |
| `solana-getStakeMinimumDelegation` | getStakeMinimumDelegation | Solana (mainnet, devnet) | [spec](spec/solana-getStakeMinimumDelegation.md) |
| `solana-getSupply` | getSupply | Solana (mainnet, devnet) | [spec](spec/solana-getSupply.md) |
| `solana-getTokenAccountBalance` | getTokenAccountBalance | Solana (mainnet, devnet) | [spec](spec/solana-getTokenAccountBalance.md) |
| `solana-getTokenAccountsByOwner` | getTokenAccountsByOwner | Solana (mainnet, devnet) | [spec](spec/solana-getTokenAccountsByOwner.md) |
| `solana-getTokenSupply` | getTokenSupply | Solana (mainnet, devnet) | [spec](spec/solana-getTokenSupply.md) |
| `solana-getTransaction` | getTransaction | Solana (mainnet, devnet) | [spec](spec/solana-getTransaction.md) |
| `solana-getTransactionCount` | getTransactionCount | Solana (mainnet, devnet) | [spec](spec/solana-getTransactionCount.md) |
| `solana-getVersion` | getVersion | Solana (mainnet, devnet) | [spec](spec/solana-getVersion.md) |
| `solana-getVoteAccounts` | getVoteAccounts | Solana (mainnet, devnet) | [spec](spec/solana-getVoteAccounts.md) |
| `solana-isBlockhashValid` | isBlockhashValid | Solana (mainnet, devnet) | [spec](spec/solana-isBlockhashValid.md) |
| `solana-minimumLedgerSlot` | minimumLedgerSlot | Solana (mainnet, devnet) | [spec](spec/solana-minimumLedgerSlot.md) |
| `solana-sendTransaction` | sendTransaction | Solana (mainnet, devnet) | [spec](spec/solana-sendTransaction.md) |
| `solana-simulateTransaction` | simulateTransaction | Solana (mainnet, devnet) | [spec](spec/solana-simulateTransaction.md) |

## Node API - Sui (JSON-RPC)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `sui-sui_devInspectTransactionBlock` | sui_devInspectTransactionBlock | Sui (mainnet, testnet) | [spec](spec/sui-sui_devInspectTransactionBlock.md) |
| `sui-sui_dryRunTransactionBlock` | sui_dryRunTransactionBlock | Sui (mainnet, testnet) | [spec](spec/sui-sui_dryRunTransactionBlock.md) |
| `sui-sui_executeTransactionBlock` | sui_executeTransactionBlock | Sui (mainnet, testnet) | [spec](spec/sui-sui_executeTransactionBlock.md) |
| `sui-sui_getChainIdentifier` | sui_getChainIdentifier | Sui (mainnet, testnet) | [spec](spec/sui-sui_getChainIdentifier.md) |
| `sui-sui_getCheckpoint` | sui_getCheckpoint | Sui (mainnet, testnet) | [spec](spec/sui-sui_getCheckpoint.md) |
| `sui-sui_getCheckpoints` | sui_getCheckpoints | Sui (mainnet, testnet) | [spec](spec/sui-sui_getCheckpoints.md) |
| `sui-sui_getEvents` | sui_getEvents | Sui (mainnet, testnet) | [spec](spec/sui-sui_getEvents.md) |
| `sui-sui_getLatestCheckpointSequenceNumber` | sui_getLatestCheckpointSequenceNumber | Sui (mainnet, testnet) | [spec](spec/sui-sui_getLatestCheckpointSequenceNumber.md) |
| `sui-sui_getMoveFunctionArgTypes` | sui_getMoveFunctionArgTypes | Sui (mainnet, testnet) | [spec](spec/sui-sui_getMoveFunctionArgTypes.md) |
| `sui-sui_getNormalizedMoveFunction` | sui_getNormalizedMoveFunction | Sui (mainnet, testnet) | [spec](spec/sui-sui_getNormalizedMoveFunction.md) |
| `sui-sui_getNormalizedMoveModule` | sui_getNormalizedMoveModule | Sui (mainnet, testnet) | [spec](spec/sui-sui_getNormalizedMoveModule.md) |
| `sui-sui_getNormalizedMoveModulesByPackage` | sui_getNormalizedMoveModulesByPackage | Sui (mainnet, testnet) | [spec](spec/sui-sui_getNormalizedMoveModulesByPackage.md) |
| `sui-sui_getNormalizedMoveStruct` | sui_getNormalizedMoveStruct | Sui (mainnet, testnet) | [spec](spec/sui-sui_getNormalizedMoveStruct.md) |
| `sui-sui_getObject` | sui_getObject | Sui (mainnet, testnet) | [spec](spec/sui-sui_getObject.md) |
| `sui-sui_getProtocolConfig` | sui_getProtocolConfig | Sui (mainnet, testnet) | [spec](spec/sui-sui_getProtocolConfig.md) |
| `sui-sui_getTotalTransactionBlocks` | sui_getTotalTransactionBlocks | Sui (mainnet, testnet) | [spec](spec/sui-sui_getTotalTransactionBlocks.md) |
| `sui-sui_getTransactionBlock` | sui_getTransactionBlock | Sui (mainnet, testnet) | [spec](spec/sui-sui_getTransactionBlock.md) |
| `sui-sui_multiGetObjects` | sui_multiGetObjects | Sui (mainnet, testnet) | [spec](spec/sui-sui_multiGetObjects.md) |
| `sui-sui_multiGetTransactionBlocks` | sui_multiGetTransactionBlocks | Sui (mainnet, testnet) | [spec](spec/sui-sui_multiGetTransactionBlocks.md) |
| `sui-sui_tryGetPastObject` | sui_tryGetPastObject | Sui (mainnet, testnet) | [spec](spec/sui-sui_tryGetPastObject.md) |
| `sui-sui_tryMultiGetPastObjects` | sui_tryMultiGetPastObjects | Sui (mainnet, testnet) | [spec](spec/sui-sui_tryMultiGetPastObjects.md) |
| `sui-sui_verifyZkLoginSignature` | sui_verifyZkLoginSignature | Sui (mainnet, testnet) | [spec](spec/sui-sui_verifyZkLoginSignature.md) |
| `sui-suix_getAllBalances` | suix_getAllBalances | Sui (mainnet, testnet) | [spec](spec/sui-suix_getAllBalances.md) |
| `sui-suix_getAllCoins` | suix_getAllCoins | Sui (mainnet, testnet) | [spec](spec/sui-suix_getAllCoins.md) |
| `sui-suix_getBalance` | suix_getBalance | Sui (mainnet, testnet) | [spec](spec/sui-suix_getBalance.md) |
| `sui-suix_getCoinMetadata` | suix_getCoinMetadata | Sui (mainnet, testnet) | [spec](spec/sui-suix_getCoinMetadata.md) |
| `sui-suix_getCoins` | suix_getCoins | Sui (mainnet, testnet) | [spec](spec/sui-suix_getCoins.md) |
| `sui-suix_getCommitteeInfo` | suix_getCommitteeInfo | Sui (mainnet, testnet) | [spec](spec/sui-suix_getCommitteeInfo.md) |
| `sui-suix_getDynamicFieldObject` | suix_getDynamicFieldObject | Sui (mainnet, testnet) | [spec](spec/sui-suix_getDynamicFieldObject.md) |
| `sui-suix_getDynamicFields` | suix_getDynamicFields | Sui (mainnet, testnet) | [spec](spec/sui-suix_getDynamicFields.md) |
| `sui-suix_getLatestSuiSystemState` | suix_getLatestSuiSystemState | Sui (mainnet, testnet) | [spec](spec/sui-suix_getLatestSuiSystemState.md) |
| `sui-suix_getOwnedObjects` | suix_getOwnedObjects | Sui (mainnet, testnet) | [spec](spec/sui-suix_getOwnedObjects.md) |
| `sui-suix_getReferenceGasPrice` | suix_getReferenceGasPrice | Sui (mainnet, testnet) | [spec](spec/sui-suix_getReferenceGasPrice.md) |
| `sui-suix_getStakes` | suix_getStakes | Sui (mainnet, testnet) | [spec](spec/sui-suix_getStakes.md) |
| `sui-suix_getStakesByIds` | suix_getStakesByIds | Sui (mainnet, testnet) | [spec](spec/sui-suix_getStakesByIds.md) |
| `sui-suix_getTotalSupply` | suix_getTotalSupply | Sui (mainnet, testnet) | [spec](spec/sui-suix_getTotalSupply.md) |
| `sui-suix_getValidatorsApy` | suix_getValidatorsApy | Sui (mainnet, testnet) | [spec](spec/sui-suix_getValidatorsApy.md) |
| `sui-suix_queryEvents` | suix_queryEvents | Sui (mainnet, testnet) | [spec](spec/sui-suix_queryEvents.md) |
| `sui-suix_queryTransactionBlocks` | suix_queryTransactionBlocks | Sui (mainnet, testnet) | [spec](spec/sui-suix_queryTransactionBlocks.md) |
| `sui-suix_resolveNameServiceAddress` | suix_resolveNameServiceAddress | Sui (mainnet, testnet) | [spec](spec/sui-suix_resolveNameServiceAddress.md) |
| `sui-suix_resolveNameServiceNames` | suix_resolveNameServiceNames | Sui (mainnet, testnet) | [spec](spec/sui-suix_resolveNameServiceNames.md) |
| `sui-suix_subscribeEvent` | suix_subscribeEvent | Sui (mainnet, testnet) | [spec](spec/sui-suix_subscribeEvent.md) |
| `sui-suix_subscribeTransaction` | suix_subscribeTransaction | Sui (mainnet, testnet) | [spec](spec/sui-suix_subscribeTransaction.md) |
| `sui-unsafe_batchTransaction` | unsafe_batchTransaction | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_batchTransaction.md) |
| `sui-unsafe_mergeCoins` | unsafe_mergeCoins | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_mergeCoins.md) |
| `sui-unsafe_moveCall` | unsafe_moveCall | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_moveCall.md) |
| `sui-unsafe_pay` | unsafe_pay | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_pay.md) |
| `sui-unsafe_payAllSui` | unsafe_payAllSui | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_payAllSui.md) |
| `sui-unsafe_paySui` | unsafe_paySui | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_paySui.md) |
| `sui-unsafe_publish` | unsafe_publish | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_publish.md) |
| `sui-unsafe_requestAddStake` | unsafe_requestAddStake | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_requestAddStake.md) |
| `sui-unsafe_requestWithdrawStake` | unsafe_requestWithdrawStake | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_requestWithdrawStake.md) |
| `sui-unsafe_splitCoin` | unsafe_splitCoin | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_splitCoin.md) |
| `sui-unsafe_splitCoinEqual` | unsafe_splitCoinEqual | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_splitCoinEqual.md) |
| `sui-unsafe_transferObject` | unsafe_transferObject | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_transferObject.md) |
| `sui-unsafe_transferSui` | unsafe_transferSui | Sui (mainnet, testnet) | [spec](spec/sui-unsafe_transferSui.md) |

## Node API - Aptos (REST)

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `aptos-encodeSubmission` | Encode submission | Aptos (mainnet, testnet) | [spec](spec/aptos-encodeSubmission.md) |
| `aptos-estimateGasPrice` | Estimate gas price | Aptos (mainnet, testnet) | [spec](spec/aptos-estimateGasPrice.md) |
| `aptos-executeViewFunctionOfAModule` | Execute view function of a module | Aptos (mainnet, testnet) | [spec](spec/aptos-executeViewFunctionOfAModule.md) |
| `aptos-getAccount` | Get account | Aptos (mainnet, testnet) | [spec](spec/aptos-getAccount.md) |
| `aptos-getAccountBalance` | Get account balance | Aptos (mainnet, testnet) | [spec](spec/aptos-getAccountBalance.md) |
| `aptos-getAccountModule` | Get account module | Aptos (mainnet, testnet) | [spec](spec/aptos-getAccountModule.md) |
| `aptos-getAccountModules` | Get account modules | Aptos (mainnet, testnet) | [spec](spec/aptos-getAccountModules.md) |
| `aptos-getAccountResource` | Get account resource | Aptos (mainnet, testnet) | [spec](spec/aptos-getAccountResource.md) |
| `aptos-getAccountResources` | Get account resources | Aptos (mainnet, testnet) | [spec](spec/aptos-getAccountResources.md) |
| `aptos-getAccountTransactions` | Get account transactions | Aptos (mainnet, testnet) | [spec](spec/aptos-getAccountTransactions.md) |
| `aptos-getBlocksByHeight` | Get blocks by height | Aptos (mainnet, testnet) | [spec](spec/aptos-getBlocksByHeight.md) |
| `aptos-getBlocksByVersion` | Get blocks by version | Aptos (mainnet, testnet) | [spec](spec/aptos-getBlocksByVersion.md) |
| `aptos-getEventsByCreationNumber` | Get events by creation number | Aptos (mainnet, testnet) | [spec](spec/aptos-getEventsByCreationNumber.md) |
| `aptos-getEventsByEventHandle` | Get events by event handle | Aptos (mainnet, testnet) | [spec](spec/aptos-getEventsByEventHandle.md) |
| `aptos-getLedgerInfo` | Get ledger info | Aptos (mainnet, testnet) | [spec](spec/aptos-getLedgerInfo.md) |
| `aptos-getRawTableItem` | Get raw table item | Aptos (mainnet, testnet) | [spec](spec/aptos-getRawTableItem.md) |
| `aptos-getTableItem` | Get table item | Aptos (mainnet, testnet) | [spec](spec/aptos-getTableItem.md) |
| `aptos-getTransactionByHash` | Get transaction by hash | Aptos (mainnet, testnet) | [spec](spec/aptos-getTransactionByHash.md) |
| `aptos-getTransactionByVersion` | Get transaction by version | Aptos (mainnet, testnet) | [spec](spec/aptos-getTransactionByVersion.md) |
| `aptos-getTransactionSummaries` | Get transaction summaries | Aptos (mainnet, testnet) | [spec](spec/aptos-getTransactionSummaries.md) |
| `aptos-getTransactions` | Get transactions | Aptos (mainnet, testnet) | [spec](spec/aptos-getTransactions.md) |
| `aptos-simulateTransaction` | Simulate transaction | Aptos (mainnet, testnet) | [spec](spec/aptos-simulateTransaction.md) |
| `aptos-submitBatchTransactions` | Submit batch transactions | Aptos (mainnet, testnet) | [spec](spec/aptos-submitBatchTransactions.md) |
| `aptos-submitTransaction` | Submit transaction | Aptos (mainnet, testnet) | [spec](spec/aptos-submitTransaction.md) |
| `aptos-waitForTransactionByHash` | Wait for transaction by hash | Aptos (mainnet, testnet) | [spec](spec/aptos-waitForTransactionByHash.md) |

## Data API - Asset

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `getAssetHoldersById` | Get Asset Holders By ID | tron | [spec](spec/getAssetHoldersById.md) |
| `getAssetMetadataByIds` | Get Asset Metadata By IDs | tron | [spec](spec/getAssetMetadataByIds.md) |
| `getAssetMetadataByIssuer` | Get Asset Metadata By Issuer | tron | [spec](spec/getAssetMetadataByIssuer.md) |
| `getAssetTransfersByAccount` | Get Asset Transfers By Account | tron | [spec](spec/getAssetTransfersByAccount.md) |
| `getAssetTransfersById` | Get Asset Transfers By ID | tron | [spec](spec/getAssetTransfersById.md) |
| `getAssetTransfersWithinRange` | Get Asset Transfers Within Range | tron | [spec](spec/getAssetTransfersWithinRange.md) |
| `getAssetsOwnedByAccount` | Get Assets Owned By Account | tron | [spec](spec/getAssetsOwnedByAccount.md) |
| `searchAssetMetadataByKeyword` | Search Asset Metadata By Keyword | tron | [spec](spec/searchAssetMetadataByKeyword.md) |

## Data API - Blockchain

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `getBlockByHashOrNumber` | Get Block by Hash or Number | aptos, arbitrum, arc, base, bnb, chiliz, ethereum, ethere... | [spec](spec/getBlockByHashOrNumber.md) |
| `getBlocksWithinRange` | Get Blocks Within Range | aptos, arbitrum, arc, base, bnb, chiliz, ethereum, ethere... | [spec](spec/getBlocksWithinRange.md) |
| `getEventsByAccount` | Get Events by Account | aptos | [spec](spec/getEventsByAccount.md) |
| `getEventsByType` | Get Events by Type | aptos | [spec](spec/getEventsByType.md) |
| `getGasPrice` | Get Gas Price | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getGasPrice.md) |
| `getInternalTransactionsByAccount` | Get Internal Transactions By Account | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getInternalTransactionsByAccount.md) |
| `getInternalTransactionsByTransactionHash` | Get Internal Transactions By Transaction Hash | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getInternalTransactionsByTransactionHash.md) |
| `getLedgerByHashOrIndex` | Get Ledger By Hash Or Index | xrpl | [spec](spec/getLedgerByHashOrIndex.md) |
| `getLedgersWithinRange` | Get Ledgers Within Range | xrpl | [spec](spec/getLedgersWithinRange.md) |
| `getNextNonceByAccount` | Get Next Nonce by Account | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNextNonceByAccount.md) |
| `getTotalTransactionCountByAccount` | Get Total Transaction Count By Account | aptos, arbitrum, arc, base, bnb, chiliz, ethereum, ethere... | [spec](spec/getTotalTransactionCountByAccount.md) |
| `getTransactionByHash` | Get Transaction By Hash | aptos, arbitrum, arc, base, bnb, chiliz, ethereum, ethere... | [spec](spec/getTransactionByHash.md) |
| `getTransactionByTransactionId` | Get Transaction By Transaction ID | bitcoin, bitcoincash, dogecoin | [spec](spec/getTransactionByTransactionId.md) |
| `getTransactionByVersion` | Get Transaction by Version | aptos | [spec](spec/getTransactionByVersion.md) |
| `getTransactionsByAccount` | Get Transactions By Account | aptos, arbitrum, arc, base, bnb, chiliz, ethereum, ethere... | [spec](spec/getTransactionsByAccount.md) |
| `getTransactionsByHashes` | Get Transactions By Hashes | aptos, arbitrum, arc, base, bnb, chiliz, ethereum, ethere... | [spec](spec/getTransactionsByHashes.md) |
| `getTransactionsByTransactionIds` | Get Transactions By Transaction IDs | bitcoin, bitcoincash, dogecoin | [spec](spec/getTransactionsByTransactionIds.md) |
| `getTransactionsByVersions` | Get Transactions By Versions | aptos | [spec](spec/getTransactionsByVersions.md) |
| `getTransactionsInBlock` | Get Transactions In Block | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getTransactionsInBlock.md) |
| `getTransactionsInLedger` | Get Transactions In Ledger | xrpl | [spec](spec/getTransactionsInLedger.md) |
| `getUnspentTransactionOutputsByAccount` | Get Unspent Transaction Outputs By Account | bitcoin, bitcoincash, dogecoin | [spec](spec/getUnspentTransactionOutputsByAccount.md) |
| `isContract` | Is Contract | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/isContract.md) |
| `searchEvents` | Search Events | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/searchEvents.md) |

## Data API - ENS

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `getAddressByEnsName` | Get Address By ENS Name | ethereum | [spec](spec/getAddressByEnsName.md) |
| `getEnsNameByAddress` | Get ENS Name By Address | ethereum | [spec](spec/getEnsNameByAddress.md) |
| `getEnsRecordByName` | Get ENS Record By Name | ethereum | [spec](spec/getEnsRecordByName.md) |
| `getEnsRecordsByAccount` | Get ENS Records By Account | ethereum | [spec](spec/getEnsRecordsByAccount.md) |

## Data API - NFT

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `getNftContractMetadataByContracts` | Get NFT Contract Metadata by Contracts | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNftContractMetadataByContracts.md) |
| `getNftContractsByAccount` | Get NFT Contracts by Account | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNftContractsByAccount.md) |
| `getNftHoldersByContract` | Get NFT Holders by Contract | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNftHoldersByContract.md) |
| `getNftHoldersByTokenId` | Get NFT Holders by Token ID | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNftHoldersByTokenId.md) |
| `getNftMetadataByContract` | Get NFT Metadata by Contract | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNftMetadataByContract.md) |
| `getNftMetadataByTokenIds` | Get NFT Metadata by Token IDs | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNftMetadataByTokenIds.md) |
| `getNftTransfersByAccount` | Get NFT Transfers By Account | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNftTransfersByAccount.md) |
| `getNftTransfersByContract` | Get NFT Transfers By Contract | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNftTransfersByContract.md) |
| `getNftTransfersByTokenId` | Get NFT Transfers By TokenId | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNftTransfersByTokenId.md) |
| `getNftTransfersWithinRange` | Get NFT Transfers Within Range | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNftTransfersWithinRange.md) |
| `getNftsOwnedByAccount` | Get NFTs Owned By Account | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNftsOwnedByAccount.md) |
| `searchNftContractMetadataByKeyword` | Search NFT Contract Metadata By Keyword | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/searchNftContractMetadataByKeyword.md) |
| `syncNftMetadata` | Sync Nft Metadata | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/syncNftMetadata.md) |

## Data API - Token

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `getNativeBalanceByAccount` | Get Native Balance by Account | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getNativeBalanceByAccount.md) |
| `getNativeHolders` | Get Native Holders | tron | [spec](spec/getNativeHolders.md) |
| `getNativeTokenBalanceByAccount` | Get Native Token Balance by Account | bitcoin, bitcoincash, dogecoin, xrpl | [spec](spec/getNativeTokenBalanceByAccount.md) |
| `getNativeTokenBalanceChangesByAccount` | Get Native Token Balance Changes By Account | xrpl | [spec](spec/getNativeTokenBalanceChangesByAccount.md) |
| `getNativeTokenTransfersByAccount` | Get Native Token Transfers By Account | bitcoin, bitcoincash, dogecoin | [spec](spec/getNativeTokenTransfersByAccount.md) |
| `getNativeTransfersByAccount` | Get Native Transfers By Account | arc, tron | [spec](spec/getNativeTransfersByAccount.md) |
| `getNativeTransfersWithinRange` | Get Native Transfers Within Range | arc, tron | [spec](spec/getNativeTransfersWithinRange.md) |
| `getTokenAccountsByAssetType` | Get Token Accounts by Asset Type | aptos | [spec](spec/getTokenAccountsByAssetType.md) |
| `getTokenAllowance` | Get Token Allowance | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getTokenAllowance.md) |
| `getTokenBalanceChangesByAccount` | Get Token Balance Changes by Account | aptos, xrpl | [spec](spec/getTokenBalanceChangesByAccount.md) |
| `getTokenBalanceChangesByAssetType` | Get Token Balance Changes by Asset Type | aptos | [spec](spec/getTokenBalanceChangesByAssetType.md) |
| `getTokenBalanceChangesWithinRange` | Get Token Balance Changes Within Range | aptos | [spec](spec/getTokenBalanceChangesWithinRange.md) |
| `getTokenContractMetadataByContracts` | Get Token Contract Metadata by Contracts | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getTokenContractMetadataByContracts.md) |
| `getTokenHoldersByContract` | Get Token Holders By Contract | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getTokenHoldersByContract.md) |
| `getTokenMetadataByAssetTypes` | Get Token Metadata by Asset Types | aptos | [spec](spec/getTokenMetadataByAssetTypes.md) |
| `getTokenPairByAssetType` | Get Token Pair by Asset Type | aptos | [spec](spec/getTokenPairByAssetType.md) |
| `getTokenPricesByContracts` | Get Token Prices by Contracts | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getTokenPricesByContracts.md) |
| `getTokenTransfersByAccount` | Get Token Transfers by Account | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getTokenTransfersByAccount.md) |
| `getTokenTransfersByContract` | Get Token Transfers by Contract | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getTokenTransfersByContract.md) |
| `getTokenTransfersByCurrencyAndIssuer` | Get Token Transfers By Currency And Issuer | xrpl | [spec](spec/getTokenTransfersByCurrencyAndIssuer.md) |
| `getTokenTransfersWithinRange` | Get Token Transfers Within Range | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getTokenTransfersWithinRange.md) |
| `getTokensOwnedByAccount` | Get Tokens Owned By Account | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getTokensOwnedByAccount.md) |
| `searchTokenContractMetadataByKeyword` | Search Token Contract Metadata by Keyword | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/searchTokenContractMetadataByKeyword.md) |

## Data API - Statistics

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `getAccountStats` | Get Account Stats | arbitrum, arc, base, bnb, chiliz, ethereum, ethereumclass... | [spec](spec/getAccountStats.md) |
| `getDailyActiveAccountsStats` | Get Daily Active Accounts Stats | ethereum, luniverse | [spec](spec/getDailyActiveAccountsStats.md) |
| `getDailyActiveAccountsStatsByContract` | Get Daily Active Accounts Stats By Contract | ethereum, luniverse | [spec](spec/getDailyActiveAccountsStatsByContract.md) |
| `getDailyTransactionsStats` | Get Daily Transactions Stats | ethereum, luniverse | [spec](spec/getDailyTransactionsStats.md) |
| `getDailyTransactionsStatsByContract` | Get Daily Transactions Stats By Contract | ethereum, luniverse | [spec](spec/getDailyTransactionsStatsByContract.md) |
| `getHourlyActiveAccountsStats` | Get Hourly Active Accounts Stats | ethereum, luniverse | [spec](spec/getHourlyActiveAccountsStats.md) |
| `getHourlyActiveAccountsStatsByContract` | Get Hourly Active Accounts Stats By Contract | ethereum, luniverse | [spec](spec/getHourlyActiveAccountsStatsByContract.md) |
| `getHourlyTransactionsStats` | Get Hourly Transactions Stats | ethereum, luniverse | [spec](spec/getHourlyTransactionsStats.md) |
| `getHourlyTransactionsStatsByContract` | Get Hourly Transactions Stats By Contract | ethereum, luniverse | [spec](spec/getHourlyTransactionsStatsByContract.md) |

## Webhook API

| operationId | Summary | Supported Chains | Reference |
|-------------|---------|-----------------|-----------|
| `createWebhook` | Create Webhook | aptos, arbitrum, arc, base, bnb, ethereum, giwa, kaia, op... | [spec](spec/createWebhook.md) |
| `deleteWebhook` | Delete Webhook | aptos, arbitrum, arc, base, bnb, ethereum, giwa, kaia, op... | [spec](spec/deleteWebhook.md) |
| `getWebhook` | Get Webhook | aptos, arbitrum, arc, base, bnb, ethereum, giwa, kaia, op... | [spec](spec/getWebhook.md) |
| `getWebhookHistory` | Get Webhook History | aptos, arbitrum, arc, base, bnb, ethereum, giwa, kaia, op... | [spec](spec/getWebhookHistory.md) |
| `updateWebhook` | Update Webhook | aptos, arbitrum, arc, base, bnb, ethereum, giwa, kaia, op... | [spec](spec/updateWebhook.md) |
