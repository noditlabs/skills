# Node API (JSON-RPC) Pricing

1 Credit = $0.000001 USDC. PPU minimum: 0.001 USDC for all methods.

Batch JSON-RPC (PPU): `Max(sum(each method cost), max(each method ppu_min_amount))`

## EVM Common Methods

Applies to: Arbitrum, Arc, Avalanche, Base, BNB, Ethereum, Giwa, Kaia, Luniverse, Optimism, Polygon

| Method                                    | Credit | PPU (USDC) |
|-------------------------------------------|--------|------------|
| `debug_traceBlockByHash`                  | 132    | 0.001      |
| `debug_traceBlockByNumber`                | 132    | 0.001      |
| `debug_traceCall`                         | 51     | 0.001      |
| `debug_traceTransaction`                  | 51     | 0.001      |
| `eth_blockNumber`                         | 2      | 0.001      |
| `eth_call`                                | 5      | 0.001      |
| `eth_chainId`                             | 1      | 0.001      |
| `eth_createAccessList`                    | 5      | 0.001      |
| `eth_estimateGas`                         | 5      | 0.001      |
| `eth_feeHistory`                          | 2      | 0.001      |
| `eth_gasPrice`                            | 2      | 0.001      |
| `eth_getBalance`                          | 6      | 0.001      |
| `eth_getBlockByHash`                      | 8      | 0.001      |
| `eth_getBlockByNumber`                    | 7      | 0.001      |
| `eth_getBlockTransactionCountByHash`      | 3      | 0.001      |
| `eth_getBlockTransactionCountByNumber`    | 3      | 0.001      |
| `eth_getCode`                             | 7      | 0.001      |
| `eth_getFilterChanges`                    | 4      | 0.001      |
| `eth_getFilterLogs`                       | 17     | 0.001      |
| `eth_getLogs`                             | 16     | 0.001      |
| `eth_getProof`                            | 5      | 0.001      |
| `eth_getStorageAt`                        | 6      | 0.001      |
| `eth_getTransactionByBlockHashAndIndex`   | 3      | 0.001      |
| `eth_getTransactionByBlockNumberAndIndex` | 3      | 0.001      |
| `eth_getTransactionByHash`                | 3      | 0.001      |
| `eth_getTransactionCount`                 | 5      | 0.001      |
| `eth_getTransactionReceipt`               | 4      | 0.001      |
| `eth_getUncleByBlockHashAndIndex`         | 4      | 0.001      |
| `eth_getUncleByBlockNumberAndIndex`       | 3      | 0.001      |
| `eth_getUncleCountByBlockHash`            | 4      | 0.001      |
| `eth_getUncleCountByBlockNumber`          | 3      | 0.001      |
| `eth_maxPriorityFeePerGas`                | 5      | 0.001      |
| `eth_newBlockFilter`                      | 4      | 0.001      |
| `eth_newFilter`                           | 4      | 0.001      |
| `eth_newPendingTransactionFilter`         | 4      | 0.001      |
| `eth_sendRawTransaction`                  | 10     | 0.001      |
| `eth_uninstallFilter`                     | 2      | 0.001      |
| `net_version`                             | 1      | 0.001      |
| `rpc_modules`                             | 1      | 0.001      |
| `web3_clientVersion`                      | 2      | 0.001      |
| `web3_sha3`                               | 2      | 0.001      |

## EVM Partial Support

| Method                 | Credit | PPU (USDC) | Not Supported                 |
|------------------------|--------|------------|-------------------------------|
| `eth_getBlockReceipts` | 7      | 0.001      | Avalanche, Luniverse, Polygon |
| `net_listening`        | 1      | 0.001      | Arbitrum                      |

## Chain-Specific Methods

### Base

| Method                   | Credit | PPU (USDC) |
|--------------------------|--------|------------|
| `optimism_outputAtBlock` | 2      | 0.001      |
| `optimism_rollupConfig`  | 2      | 0.001      |

### Ethereum

| Method                          | Credit | PPU (USDC) |
|---------------------------------|--------|------------|
| `trace_block`                   | 28     | 0.001      |
| `trace_call`                    | 18     | 0.001      |
| `trace_filter`                  | 18     | 0.001      |
| `trace_get`                     | 17     | 0.001      |
| `trace_replayBlockTransactions` | 29     | 0.001      |
| `trace_replayTransaction`       | 17     | 0.001      |
| `trace_transaction`             | 18     | 0.001      |

### Giwa

| Method                   | Credit | PPU (USDC) |
|--------------------------|--------|------------|
| `optimism_outputAtBlock` | 2      | 0.001      |
| `optimism_rollupConfig`  | 2      | 0.001      |

### Kaia

| Method                                     | Credit | PPU (USDC) |
|--------------------------------------------|--------|------------|
| `kaia_blockNumber`                         | 2      | 0.001      |
| `kaia_call`                                | 5      | 0.001      |
| `kaia_chainID`                             | 1      | 0.001      |
| `kaia_createAccessList`                    | 5      | 0.001      |
| `kaia_estimateGas`                         | 5      | 0.001      |
| `kaia_feeHistory`                          | 2      | 0.001      |
| `kaia_gasPrice`                            | 2      | 0.001      |
| `kaia_getBalance`                          | 6      | 0.001      |
| `kaia_getBlockByHash`                      | 8      | 0.001      |
| `kaia_getBlockByNumber`                    | 7      | 0.001      |
| `kaia_getBlockReceipts`                    | 7      | 0.001      |
| `kaia_getBlockTransactionCountByHash`      | 3      | 0.001      |
| `kaia_getBlockTransactionCountByNumber`    | 3      | 0.001      |
| `kaia_getCode`                             | 7      | 0.001      |
| `kaia_getFilterChanges`                    | 4      | 0.001      |
| `kaia_getFilterLogs`                       | 17     | 0.001      |
| `kaia_getLogs`                             | 16     | 0.001      |
| `kaia_getProof`                            | 5      | 0.001      |
| `kaia_getRewards`                          | 7      | 0.001      |
| `kaia_getStorageAt`                        | 6      | 0.001      |
| `kaia_getTransactionByBlockHashAndIndex`   | 3      | 0.001      |
| `kaia_getTransactionByBlockNumberAndIndex` | 3      | 0.001      |
| `kaia_getTransactionByHash`                | 3      | 0.001      |
| `kaia_getTransactionCount`                 | 5      | 0.001      |
| `kaia_getTransactionReceipt`               | 4      | 0.001      |
| `kaia_maxPriorityFeePerGas`                | 5      | 0.001      |
| `kaia_newBlockFilter`                      | 4      | 0.001      |
| `kaia_newFilter`                           | 4      | 0.001      |
| `kaia_newPendingTransactionFilter`         | 4      | 0.001      |
| `kaia_sendRawTransaction`                  | 10     | 0.001      |
| `kaia_uninstallFilter`                     | 2      | 0.001      |
| `klay_blockNumber`                         | 2      | 0.001      |
| `klay_call`                                | 5      | 0.001      |
| `klay_chainID`                             | 1      | 0.001      |
| `klay_createAccessList`                    | 5      | 0.001      |
| `klay_estimateGas`                         | 5      | 0.001      |
| `klay_feeHistory`                          | 2      | 0.001      |
| `klay_gasPrice`                            | 2      | 0.001      |
| `klay_getBalance`                          | 6      | 0.001      |
| `klay_getBlockByHash`                      | 8      | 0.001      |
| `klay_getBlockByNumber`                    | 7      | 0.001      |
| `klay_getBlockReceipts`                    | 7      | 0.001      |
| `klay_getBlockTransactionCountByHash`      | 3      | 0.001      |
| `klay_getBlockTransactionCountByNumber`    | 3      | 0.001      |
| `klay_getCode`                             | 7      | 0.001      |
| `klay_getFilterChanges`                    | 4      | 0.001      |
| `klay_getFilterLogs`                       | 17     | 0.001      |
| `klay_getLogs`                             | 16     | 0.001      |
| `klay_getProof`                            | 5      | 0.001      |
| `klay_getStorageAt`                        | 6      | 0.001      |
| `klay_getTransactionByBlockHashAndIndex`   | 3      | 0.001      |
| `klay_getTransactionByBlockNumberAndIndex` | 3      | 0.001      |
| `klay_getTransactionByHash`                | 3      | 0.001      |
| `klay_getTransactionCount`                 | 5      | 0.001      |
| `klay_getTransactionReceipt`               | 4      | 0.001      |
| `klay_maxPriorityFeePerGas`                | 5      | 0.001      |
| `klay_newBlockFilter`                      | 4      | 0.001      |
| `klay_newFilter`                           | 4      | 0.001      |
| `klay_newPendingTransactionFilter`         | 4      | 0.001      |
| `klay_sendRawTransaction`                  | 10     | 0.001      |
| `klay_uninstallFilter`                     | 2      | 0.001      |

### Optimism

| Method                   | Credit | PPU (USDC) |
|--------------------------|--------|------------|
| `optimism_outputAtBlock` | 2      | 0.001      |
| `optimism_rollupConfig`  | 2      | 0.001      |

### Polygon

| Method                       | Credit | PPU (USDC) |
|------------------------------|--------|------------|
| `bor_getAuthor`              | 2      | 0.001      |
| `bor_getCurrentProposer`     | 2      | 0.001      |
| `bor_getCurrentValidators`   | 2      | 0.001      |
| `bor_getSignersAtHash`       | 2      | 0.001      |

### Solana

| Method                                | Credit | PPU (USDC) |
|---------------------------------------|--------|------------|
| `getAccountInfo`                      | 5      | 0.001      |
| `getBalance`                          | 7      | 0.001      |
| `getBlock`                            | 37     | 0.001      |
| `getBlockCommitment`                  | 5      | 0.001      |
| `getBlockHeight`                      | 2      | 0.001      |
| `getBlockProduction`                  | 7      | 0.001      |
| `getBlockTime`                        | 2      | 0.001      |
| `getBlocks`                           | 7      | 0.001      |
| `getBlocksWithLimit`                  | 7      | 0.001      |
| `getClusterNodes`                     | 5      | 0.001      |
| `getEpochInfo`                        | 2      | 0.001      |
| `getEpochSchedule`                    | 2      | 0.001      |
| `getFeeForMessage`                    | 5      | 0.001      |
| `getFirstAvailableBlock`              | 2      | 0.001      |
| `getGenesisHash`                      | 2      | 0.001      |
| `getHealth`                           | 1      | 0.001      |
| `getHighestSnapshotSlot`              | 2      | 0.001      |
| `getIdentity`                         | 2      | 0.001      |
| `getInflationGovernor`                | 2      | 0.001      |
| `getInflationRate`                    | 2      | 0.001      |
| `getInflationReward`                  | 7      | 0.001      |
| `getLatestBlockhash`                  | 2      | 0.001      |
| `getLeaderSchedule`                   | 12     | 0.001      |
| `getMaxRetransmitSlot`                | 2      | 0.001      |
| `getMaxShredInsertSlot`               | 2      | 0.001      |
| `getMinimumBalanceForRentExemption`   | 2      | 0.001      |
| `getMultipleAccounts`                 | 7      | 0.001      |
| `getProgramAccounts`                  | 37     | 0.001      |
| `getRecentPerformanceSamples`         | 2      | 0.001      |
| `getRecentPrioritizationFees`         | 5      | 0.001      |
| `getSignatureStatuses`                | 5      | 0.001      |
| `getSignaturesForAddress`             | 10     | 0.001      |
| `getSlot`                             | 2      | 0.001      |
| `getSlotLeader`                       | 2      | 0.001      |
| `getSlotLeaders`                      | 2      | 0.001      |
| `getStakeMinimumDelegation`           | 2      | 0.001      |
| `getSupply`                           | 125    | 0.001      |
| `getTokenAccountBalance`              | 5      | 0.001      |
| `getTokenAccountsByOwner`             | 37     | 0.001      |
| `getTokenSupply`                      | 5      | 0.001      |
| `getTransaction`                      | 12     | 0.001      |
| `getTransactionCount`                 | 5      | 0.001      |
| `getVersion`                          | 2      | 0.001      |
| `getVoteAccounts`                     | 5      | 0.001      |
| `isBlockhashValid`                    | 5      | 0.001      |
| `minimumLedgerSlot`                   | 2      | 0.001      |
| `sendTransaction`                     | 5      | 0.001      |
| `simulateTransaction`                 | 25     | 0.001      |

### Sui

| Method                                  | Credit | PPU (USDC) |
|-----------------------------------------|--------|------------|
| `sui_devInspectTransactionBlock`        | 132    | 0.001      |
| `sui_dryRunTransactionBlock`            | 132    | 0.001      |
| `sui_executeTransactionBlock`           | 57     | 0.001      |
| `sui_getChainIdentifier`                | 1      | 0.001      |
| `sui_getCheckpoint`                     | 2      | 0.001      |
| `sui_getCheckpoints`                    | 12     | 0.001      |
| `sui_getEvents`                         | 12     | 0.001      |
| `sui_getLatestCheckpointSequenceNumber` | 1      | 0.001      |
| `sui_getMoveFunctionArgTypes`           | 12     | 0.001      |
| `sui_getNormalizedMoveFunction`         | 12     | 0.001      |
| `sui_getNormalizedMoveModule`           | 12     | 0.001      |
| `sui_getNormalizedMoveModulesByPackage` | 12     | 0.001      |
| `sui_getNormalizedMoveStruct`           | 12     | 0.001      |
| `sui_getObject`                         | 5      | 0.001      |
| `sui_getProtocolConfig`                 | 2      | 0.001      |
| `sui_getTotalTransactionBlocks`         | 2      | 0.001      |
| `sui_getTransactionBlock`               | 7      | 0.001      |
| `sui_multiGetObjects`                   | 12     | 0.001      |
| `sui_multiGetTransactionBlocks`         | 25     | 0.001      |
| `sui_tryGetPastObject`                  | 12     | 0.001      |
| `sui_tryMultiGetPastObjects`            | 25     | 0.001      |
| `sui_verifyZkLoginSignature`            | 62     | 0.001      |
| `suix_getAllBalances`                   | 7      | 0.001      |
| `suix_getAllCoins`                      | 12     | 0.001      |
| `suix_getBalance`                       | 2      | 0.001      |
| `suix_getCoinMetadata`                  | 2      | 0.001      |
| `suix_getCoins`                         | 12     | 0.001      |
| `suix_getCommitteeInfo`                 | 5      | 0.001      |
| `suix_getDynamicFieldObject`            | 12     | 0.001      |
| `suix_getDynamicFields`                 | 12     | 0.001      |
| `suix_getLatestSuiSystemState`          | 5      | 0.001      |
| `suix_getOwnedObjects`                  | 62     | 0.001      |
| `suix_getReferenceGasPrice`             | 2      | 0.001      |
| `suix_getStakes`                        | 7      | 0.001      |
| `suix_getStakesByIds`                   | 12     | 0.001      |
| `suix_getTotalSupply`                   | 2      | 0.001      |
| `suix_getValidatorsApy`                 | 7      | 0.001      |
| `suix_queryEvents`                      | 87     | 0.001      |
| `suix_queryTransactionBlocks`           | 87     | 0.001      |
| `suix_resolveNameServiceAddress`        | 7      | 0.001      |
| `suix_resolveNameServiceNames`          | 7      | 0.001      |
| `unsafe_batchTransaction`               | 87     | 0.001      |
| `unsafe_mergeCoins`                     | 87     | 0.001      |
| `unsafe_moveCall`                       | 37     | 0.001      |
| `unsafe_pay`                            | 87     | 0.001      |
| `unsafe_payAllSui`                      | 87     | 0.001      |
| `unsafe_paySui`                         | 87     | 0.001      |
| `unsafe_publish`                        | 25     | 0.001      |
| `unsafe_requestAddStake`                | 7      | 0.001      |
| `unsafe_requestWithdrawStake`           | 7      | 0.001      |
| `unsafe_splitCoin`                      | 7      | 0.001      |
| `unsafe_splitCoinEqual`                 | 7      | 0.001      |
| `unsafe_transferObject`                 | 5      | 0.001      |
| `unsafe_transferSui`                    | 5      | 0.001      |
