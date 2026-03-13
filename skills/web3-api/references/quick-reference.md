# Quick Reference

Find operations by operationId, then read the file in the Reference column for detailed specs.

## Data API - Asset Queries

| Task | Description | operationId | Supported Chains | Reference |
|------|-------------|-------------|----------|-----------|
| Token Holdings | Retrieve list of ERC-20/TRC-20 tokens and balances held by an account | `getTokensOwnedByAccount` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron, Aptos | [getTokensOwnedByAccount.md](spec/getTokensOwnedByAccount.md) |
| NFT Holdings | Retrieve full list of NFTs (ERC-721/1155) held by an account | `getNftsOwnedByAccount` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNftsOwnedByAccount.md](spec/getNftsOwnedByAccount.md) |
| Native Balance | Retrieve native token (ETH, BNB, etc.) balance of an account | `getNativeBalanceByAccount` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron | [getNativeBalanceByAccount.md](spec/getNativeBalanceByAccount.md) |
| Native Balance (UTXO) | Retrieve native token balance on UTXO-based chains | `getNativeTokenBalanceByAccount` | Bitcoin, Dogecoin, Bitcoin Cash, XRPL | [getNativeTokenBalanceByAccount.md](spec/getNativeTokenBalanceByAccount.md) |
| Token Price | Retrieve token price (USD) by contract address | `getTokenPricesByContracts` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getTokenPricesByContracts.md](spec/getTokenPricesByContracts.md) |
| Token Allowance | Retrieve token allowance approved for a spender | `getTokenAllowance` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron | [getTokenAllowance.md](spec/getTokenAllowance.md) |
| Token Contract Metadata | Retrieve metadata (name, symbol, decimals, etc.) of a token contract | `getTokenContractMetadataByContracts` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron | [getTokenContractMetadataByContracts.md](spec/getTokenContractMetadataByContracts.md) |
| NFT Metadata (Token ID) | Retrieve NFT metadata (image, attributes, etc.) for a specific tokenId | `getNftMetadataByTokenIds` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNftMetadataByTokenIds.md](spec/getNftMetadataByTokenIds.md) |
| NFT Holdings by Contract | Retrieve NFTs held by an account grouped by contract | `getNftContractsByAccount` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNftContractsByAccount.md](spec/getNftContractsByAccount.md) |
| NFT Contract Metadata | Retrieve NFT contract metadata (name, symbol, totalSupply, etc.) | `getNftContractMetadataByContracts` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNftContractMetadataByContracts.md](spec/getNftContractMetadataByContracts.md) |
| NFT Metadata List by Contract | Paginated retrieval of all token metadata within a specific NFT contract | `getNftMetadataByContract` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNftMetadataByContract.md](spec/getNftMetadataByContract.md) |
| NFT Metadata Sync | Force refresh NFT metadata to the latest state | `syncNftMetadata` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [syncNftMetadata.md](spec/syncNftMetadata.md) |
| Token Metadata (Aptos) | Retrieve token metadata by Aptos asset type | `getTokenMetadataByAssetTypes` | Aptos | [getTokenMetadataByAssetTypes.md](spec/getTokenMetadataByAssetTypes.md) |
| Token Accounts (Aptos) | Retrieve list of accounts holding a specific asset type | `getTokenAccountsByAssetType` | Aptos | [getTokenAccountsByAssetType.md](spec/getTokenAccountsByAssetType.md) |
| Token Pair (Aptos) | Retrieve Aptos DEX token pair information | `getTokenPairByAssetType` | Aptos | [getTokenPairByAssetType.md](spec/getTokenPairByAssetType.md) |

## Data API - Transfers / History

| Task | Description | operationId | Supported Chains | Reference |
|------|-------------|-------------|----------|-----------|
| Token Transfer History (Account) | Retrieve full token send/receive history for an account | `getTokenTransfersByAccount` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron, XRPL | [getTokenTransfersByAccount.md](spec/getTokenTransfersByAccount.md) |
| Token Transfer History (Contract) | Retrieve full transfer history for a specific token contract | `getTokenTransfersByContract` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron | [getTokenTransfersByContract.md](spec/getTokenTransfersByContract.md) |
| Token Transfer History (Range) | Retrieve token transfer history by block range | `getTokenTransfersWithinRange` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron, XRPL | [getTokenTransfersWithinRange.md](spec/getTokenTransfersWithinRange.md) |
| Token Transfer History (Currency/Issuer) | Retrieve transfer history by XRPL currency code + issuer | `getTokenTransfersByCurrencyAndIssuer` | XRPL | [getTokenTransfersByCurrencyAndIssuer.md](spec/getTokenTransfersByCurrencyAndIssuer.md) |
| NFT Transfer History (Account) | Retrieve full NFT send/receive history for an account | `getNftTransfersByAccount` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNftTransfersByAccount.md](spec/getNftTransfersByAccount.md) |
| NFT Transfer History (Contract) | Retrieve full transfer history for a specific NFT contract | `getNftTransfersByContract` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNftTransfersByContract.md](spec/getNftTransfersByContract.md) |
| NFT Transfer History (Token ID) | Track ownership transfer history for a specific NFT tokenId | `getNftTransfersByTokenId` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNftTransfersByTokenId.md](spec/getNftTransfersByTokenId.md) |
| NFT Transfer History (Range) | Retrieve NFT transfer history by block range | `getNftTransfersWithinRange` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNftTransfersWithinRange.md](spec/getNftTransfersWithinRange.md) |
| Native Transfer History | Retrieve native token (TRX) send/receive history for an account | `getNativeTransfersByAccount` | Tron | [getNativeTransfersByAccount.md](spec/getNativeTransfersByAccount.md) |
| Native Transfers (Range) | Retrieve native token transfer history by block range | `getNativeTransfersWithinRange` | Tron | [getNativeTransfersWithinRange.md](spec/getNativeTransfersWithinRange.md) |
| UTXO Transfers | Retrieve native token transfer history on UTXO-based chains | `getNativeTokenTransfersByAccount` | Bitcoin, Dogecoin, Bitcoin Cash | [getNativeTokenTransfersByAccount.md](spec/getNativeTokenTransfersByAccount.md) |
| Internal Tx (Account) | Retrieve internal transactions (contract-to-contract calls) for an account | `getInternalTransactionsByAccount` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron | [getInternalTransactionsByAccount.md](spec/getInternalTransactionsByAccount.md) |
| Internal Tx (Hash) | Retrieve list of internal transactions within a specific transaction | `getInternalTransactionsByTransactionHash` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron | [getInternalTransactionsByTransactionHash.md](spec/getInternalTransactionsByTransactionHash.md) |
| Token Balance Changes (Account) | Retrieve token balance change history for an account | `getTokenBalanceChangesByAccount` | XRPL, Aptos | [getTokenBalanceChangesByAccount.md](spec/getTokenBalanceChangesByAccount.md) |
| Token Balance Changes (AssetType) | Retrieve balance change history for a specific asset type | `getTokenBalanceChangesByAssetType` | Aptos | [getTokenBalanceChangesByAssetType.md](spec/getTokenBalanceChangesByAssetType.md) |
| Token Balance Changes (Range) | Retrieve balance change history by block/version range | `getTokenBalanceChangesWithinRange` | Aptos | [getTokenBalanceChangesWithinRange.md](spec/getTokenBalanceChangesWithinRange.md) |
| Native Balance Changes | Retrieve XRP balance change history for an XRPL account | `getNativeTokenBalanceChangesByAccount` | XRPL | [getNativeTokenBalanceChangesByAccount.md](spec/getNativeTokenBalanceChangesByAccount.md) |

## Data API - Blocks / Transactions

| Task | Description | operationId | Supported Chains | Reference |
|------|-------------|-------------|----------|-----------|
| Block Query | Retrieve detailed information for a single block by hash or number | `getBlockByHashOrNumber` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Bitcoin, Aptos | [getBlockByHashOrNumber.md](spec/getBlockByHashOrNumber.md) |
| Block List (Range) | Paginated retrieval of blocks by block number range | `getBlocksWithinRange` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Aptos | [getBlocksWithinRange.md](spec/getBlocksWithinRange.md) |
| Transaction Query (Hash) | Retrieve detailed information for a single transaction by hash | `getTransactionByHash` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, XRPL, Aptos | [getTransactionByHash.md](spec/getTransactionByHash.md) |
| Transaction Query (UTXO) | Retrieve a single transaction by UTXO transaction ID | `getTransactionByTransactionId` | Bitcoin, Dogecoin, Bitcoin Cash | [getTransactionByTransactionId.md](spec/getTransactionByTransactionId.md) |
| Transaction Query (Version) | Retrieve a single transaction by Aptos version number | `getTransactionByVersion` | Aptos | [getTransactionByVersion.md](spec/getTransactionByVersion.md) |
| Account Transaction List | Paginated retrieval of full transaction history for an account | `getTransactionsByAccount` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron, Bitcoin, Dogecoin, Bitcoin Cash, XRPL, Aptos | [getTransactionsByAccount.md](spec/getTransactionsByAccount.md) |
| Batch Transaction Query (Hash) | Batch query multiple transaction hashes at once | `getTransactionsByHashes` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, XRPL, Aptos | [getTransactionsByHashes.md](spec/getTransactionsByHashes.md) |
| Batch Transaction Query (UTXO) | Batch query multiple UTXO transaction IDs at once | `getTransactionsByTransactionIds` | Bitcoin, Dogecoin, Bitcoin Cash | [getTransactionsByTransactionIds.md](spec/getTransactionsByTransactionIds.md) |
| Batch Transaction Query (Version) | Batch query multiple Aptos versions at once | `getTransactionsByVersions` | Aptos | [getTransactionsByVersions.md](spec/getTransactionsByVersions.md) |
| Transactions in Block | Retrieve list of transactions included in a specific block | `getTransactionsInBlock` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron, Aptos | [getTransactionsInBlock.md](spec/getTransactionsInBlock.md) |
| Transactions in Ledger | Retrieve list of transactions included in a specific XRPL ledger | `getTransactionsInLedger` | XRPL | [getTransactionsInLedger.md](spec/getTransactionsInLedger.md) |
| Total Transaction Count | Retrieve total number of transactions initiated by an account | `getTotalTransactionCountByAccount` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron, Bitcoin, Dogecoin, Bitcoin Cash, XRPL, Aptos | [getTotalTransactionCountByAccount.md](spec/getTotalTransactionCountByAccount.md) |
| Gas Price | Retrieve current average network gas price | `getGasPrice` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getGasPrice.md](spec/getGasPrice.md) |
| Next Nonce | Retrieve next available nonce value for an account | `getNextNonceByAccount` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNextNonceByAccount.md](spec/getNextNonceByAccount.md) |
| Is Contract | Determine whether an address is an EOA or contract | `isContract` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron | [isContract.md](spec/isContract.md) |
| Event Search | Search on-chain event logs by topic/contract | `searchEvents` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [searchEvents.md](spec/searchEvents.md) |
| UTXO List | Retrieve unspent transaction outputs (UTXOs) for an account | `getUnspentTransactionOutputsByAccount` | Bitcoin, Dogecoin, Bitcoin Cash | [getUnspentTransactionOutputsByAccount.md](spec/getUnspentTransactionOutputsByAccount.md) |
| Ledger Query | Retrieve a single XRPL ledger by hash or index | `getLedgerByHashOrIndex` | XRPL | [getLedgerByHashOrIndex.md](spec/getLedgerByHashOrIndex.md) |
| Ledger List (Range) | Retrieve list of ledgers by ledger index range | `getLedgersWithinRange` | XRPL | [getLedgersWithinRange.md](spec/getLedgersWithinRange.md) |

## Data API - Holders / Search / Statistics

| Task | Description | operationId | Supported Chains | Reference |
|------|-------------|-------------|----------|-----------|
| Token Holders | Retrieve holder list and balances for a specific token contract | `getTokenHoldersByContract` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron | [getTokenHoldersByContract.md](spec/getTokenHoldersByContract.md) |
| NFT Holders (Contract) | Retrieve full holder list for an NFT contract | `getNftHoldersByContract` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNftHoldersByContract.md](spec/getNftHoldersByContract.md) |
| NFT Holders (Token ID) | Retrieve current/past owners of a specific NFT tokenId | `getNftHoldersByTokenId` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [getNftHoldersByTokenId.md](spec/getNftHoldersByTokenId.md) |
| Native Holders | Retrieve top TRX holders list | `getNativeHolders` | Tron | [getNativeHolders.md](spec/getNativeHolders.md) |
| Token Search | Search token contract metadata by keyword | `searchTokenContractMetadataByKeyword` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron | [searchTokenContractMetadataByKeyword.md](spec/searchTokenContractMetadataByKeyword.md) |
| NFT Search | Search NFT contract metadata by keyword | `searchNftContractMetadataByKeyword` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic | [searchNftContractMetadataByKeyword.md](spec/searchNftContractMetadataByKeyword.md) |
| Account Statistics | Summary statistics for an account (first transaction date, total count, etc.) | `getAccountStats` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Chiliz, Ethereum Classic, Tron, Aptos | [getAccountStats.md](spec/getAccountStats.md) |
| Daily Active Accounts | Daily active account count statistics for the entire network | `getDailyActiveAccountsStats` | Ethereum, Luniverse | [getDailyActiveAccountsStats.md](spec/getDailyActiveAccountsStats.md) |
| Daily Active Accounts (Contract) | Daily active account count that interacted with a specific contract | `getDailyActiveAccountsStatsByContract` | Ethereum, Luniverse | [getDailyActiveAccountsStatsByContract.md](spec/getDailyActiveAccountsStatsByContract.md) |
| Daily Transactions | Daily transaction count statistics for the entire network | `getDailyTransactionsStats` | Ethereum, Luniverse | [getDailyTransactionsStats.md](spec/getDailyTransactionsStats.md) |
| Daily Transactions (Contract) | Daily transaction count statistics for a specific contract | `getDailyTransactionsStatsByContract` | Ethereum, Luniverse | [getDailyTransactionsStatsByContract.md](spec/getDailyTransactionsStatsByContract.md) |
| Hourly Active Accounts | Hourly active account count statistics for the entire network | `getHourlyActiveAccountsStats` | Ethereum, Luniverse | [getHourlyActiveAccountsStats.md](spec/getHourlyActiveAccountsStats.md) |
| Hourly Active Accounts (Contract) | Hourly active account count that interacted with a specific contract | `getHourlyActiveAccountsStatsByContract` | Ethereum, Luniverse | [getHourlyActiveAccountsStatsByContract.md](spec/getHourlyActiveAccountsStatsByContract.md) |
| Hourly Transactions | Hourly transaction count statistics for the entire network | `getHourlyTransactionsStats` | Ethereum, Luniverse | [getHourlyTransactionsStats.md](spec/getHourlyTransactionsStats.md) |
| Hourly Transactions (Contract) | Hourly transaction count statistics for a specific contract | `getHourlyTransactionsStatsByContract` | Ethereum, Luniverse | [getHourlyTransactionsStatsByContract.md](spec/getHourlyTransactionsStatsByContract.md) |
| ENS → Address | Retrieve wallet address mapped to an ENS name | `getAddressByEnsName` | Ethereum | [getAddressByEnsName.md](spec/getAddressByEnsName.md) |
| Address → ENS | Reverse lookup of ENS name associated with a wallet address | `getEnsNameByAddress` | Ethereum | [getEnsNameByAddress.md](spec/getEnsNameByAddress.md) |
| ENS Record (Name) | Retrieve ENS name details including resolver and text records | `getEnsRecordByName` | Ethereum | [getEnsRecordByName.md](spec/getEnsRecordByName.md) |
| ENS Records (Account) | Retrieve list of ENS names and records owned by an account | `getEnsRecordsByAccount` | Ethereum | [getEnsRecordsByAccount.md](spec/getEnsRecordsByAccount.md) |

## Data API - Tron TRC-10 Asset

| Task | Description | operationId | Supported Chains | Reference |
|------|-------------|-------------|----------|-----------|
| Asset Holdings | Retrieve list of TRC-10 assets and balances held by an account | `getAssetsOwnedByAccount` | Tron | [getAssetsOwnedByAccount.md](spec/getAssetsOwnedByAccount.md) |
| Asset Holders | Retrieve holder list for a specific TRC-10 asset ID | `getAssetHoldersById` | Tron | [getAssetHoldersById.md](spec/getAssetHoldersById.md) |
| Asset Metadata (ID) | Retrieve metadata by TRC-10 asset ID | `getAssetMetadataByIds` | Tron | [getAssetMetadataByIds.md](spec/getAssetMetadataByIds.md) |
| Asset Metadata (Issuer) | Retrieve TRC-10 asset metadata by issuer address | `getAssetMetadataByIssuer` | Tron | [getAssetMetadataByIssuer.md](spec/getAssetMetadataByIssuer.md) |
| Asset Transfers (Account) | Retrieve TRC-10 asset transfer history for an account | `getAssetTransfersByAccount` | Tron | [getAssetTransfersByAccount.md](spec/getAssetTransfersByAccount.md) |
| Asset Transfers (ID) | Retrieve full transfer history for a specific TRC-10 asset ID | `getAssetTransfersById` | Tron | [getAssetTransfersById.md](spec/getAssetTransfersById.md) |
| Asset Transfers (Range) | Retrieve TRC-10 asset transfer history by block range | `getAssetTransfersWithinRange` | Tron | [getAssetTransfersWithinRange.md](spec/getAssetTransfersWithinRange.md) |
| Asset Search | Search TRC-10 asset metadata by keyword | `searchAssetMetadataByKeyword` | Tron | [searchAssetMetadataByKeyword.md](spec/searchAssetMetadataByKeyword.md) |

## Node API - Key Methods

| Task | Description | operationId | Supported Chains | Reference |
|------|-------------|-------------|----------|-----------|
| Balance Query | Retrieve account native balance (wei) at a specific block | `eth_getBalance` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_getBalance.md](spec/eth_getBalance.md) |
| Contract Call | Read-only smart contract function call without state changes | `eth_call` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_call.md](spec/eth_call.md) |
| Gas Estimation | Pre-estimate gas required to execute a transaction | `eth_estimateGas` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_estimateGas.md](spec/eth_estimateGas.md) |
| Block Number | Retrieve current latest block number | `eth_blockNumber` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_blockNumber.md](spec/eth_blockNumber.md) |
| Block Query (Number) | Retrieve block header and transactions by block number | `eth_getBlockByNumber` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_getBlockByNumber.md](spec/eth_getBlockByNumber.md) |
| Block Query (Hash) | Retrieve block header and transactions by block hash | `eth_getBlockByHash` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_getBlockByHash.md](spec/eth_getBlockByHash.md) |
| Log Query | Retrieve event logs filtered by address/topics | `eth_getLogs` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_getLogs.md](spec/eth_getLogs.md) |
| Tx Query | Retrieve transaction details by transaction hash | `eth_getTransactionByHash` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_getTransactionByHash.md](spec/eth_getTransactionByHash.md) |
| Tx Receipt | Retrieve transaction execution result (status, logs, gasUsed) | `eth_getTransactionReceipt` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_getTransactionReceipt.md](spec/eth_getTransactionReceipt.md) |
| Tx Send | Broadcast a signed transaction to the network | `eth_sendRawTransaction` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_sendRawTransaction.md](spec/eth_sendRawTransaction.md) |
| Tx Trace | Opcode-level debug trace of transaction execution | `debug_traceTransaction` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [debug_traceTransaction.md](spec/debug_traceTransaction.md) |
| Gas Price | Retrieve current network gas price (wei) | `eth_gasPrice` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_gasPrice.md](spec/eth_gasPrice.md) |
| Code Query | Retrieve deployed bytecode at a contract address | `eth_getCode` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_getCode.md](spec/eth_getCode.md) |
| Storage Query | Retrieve value at a specific storage slot of a contract | `eth_getStorageAt` | Ethereum, Arbitrum, Base, Optimism, Polygon, BNB, Kaia, Luniverse, Giwa, Arc | [eth_getStorageAt.md](spec/eth_getStorageAt.md) |

**operationId rules (Node API):**
- Ethereum: no prefix (`eth_blockNumber`)
- Other chains: `{chain}-{method}` (`polygon-eth_blockNumber`, `solana-getBalance`, `sui-sui_getObject`)

For the full Node API list, see the `references/` directory for `eth_*.md`, `debug_*.md`, `trace_*.md`, `solana-*.md`, `sui-*.md`, `kaia-*.md`, etc.

## Aptos Indexer (GraphQL)

| Task | Description | Query Root | Supported Chains | Reference |
|------|-------------|-----------|----------|-----------|
| Current Coin Balance | Retrieve current coin balance snapshot for an account | `current_coin_balances` | Aptos | [aptos-indexer-current_coin_balances.md](spec/aptos-indexer-current_coin_balances.md) |
| Coin Activity History | Retrieve history of coin activity events (deposits, withdrawals, swaps, etc.) | `coin_activities` | Aptos | [aptos-indexer-coin_activities.md](spec/aptos-indexer-coin_activities.md) |
| Coin Balance Snapshot | Retrieve coin balance history at a specific version | `coin_balances` | Aptos | [aptos-indexer-coin_balances.md](spec/aptos-indexer-coin_balances.md) |
| Coin Metadata | Retrieve name, symbol, decimals metadata by coin type | `coin_infos` | Aptos | [aptos-indexer-coin_infos.md](spec/aptos-indexer-coin_infos.md) |
| Current Token Ownership | Retrieve current NFT/token ownership status for an account | `current_token_ownerships` | Aptos | [aptos-indexer-current_token_ownerships.md](spec/aptos-indexer-current_token_ownerships.md) |
| Current Token Data | Retrieve current token metadata (URI, supply, etc.) | `current_token_datas` | Aptos | [aptos-indexer-current_token_datas.md](spec/aptos-indexer-current_token_datas.md) |
| Token Activity History | Retrieve token activity events (minting, transfers, burns, etc.) | `token_activities` | Aptos | [aptos-indexer-token_activities.md](spec/aptos-indexer-token_activities.md) |
| Token Data History | Retrieve version-by-version change history of token metadata | `token_datas` | Aptos | [aptos-indexer-token_datas.md](spec/aptos-indexer-token_datas.md) |
| Token Ownership History | Track version-by-version changes in token ownership | `token_ownerships` | Aptos | [aptos-indexer-token_ownerships.md](spec/aptos-indexer-token_ownerships.md) |
| Token Instance | Retrieve detailed information for individual token instances | `tokens` | Aptos | [aptos-indexer-tokens.md](spec/aptos-indexer-tokens.md) |
| Collection Data History | Retrieve version-by-version metadata change history for an NFT collection | `collection_datas` | Aptos | [aptos-indexer-collection_datas.md](spec/aptos-indexer-collection_datas.md) |
| Current Collection Data | Retrieve current metadata for an NFT collection | `current_collection_datas` | Aptos | [aptos-indexer-current_collection_datas.md](spec/aptos-indexer-current_collection_datas.md) |
| Aptos Name Service | Retrieve ANS name ↔ address mapping | `current_ans_lookup` | Aptos | [aptos-indexer-current_ans_lookup.md](spec/aptos-indexer-current_ans_lookup.md) |
| Move Resources | Retrieve Move resources (module state) for an account | `move_resources` | Aptos | [aptos-indexer-move_resources.md](spec/aptos-indexer-move_resources.md) |
| Address-Version Mapping | Retrieve address-version pairs where Move resource changes occurred | `address_version_from_move_resources` | Aptos | [aptos-indexer-address_version_from_move_resources.md](spec/aptos-indexer-address_version_from_move_resources.md) |

## Webhook

| Task | Description | operationId | Supported Chains | Reference |
|------|-------------|-------------|----------|-----------|
| Create | Create a webhook to receive HTTP callbacks when on-chain events are detected | `createWebhook` | Arbitrum, Base, BNB, Ethereum, Giwa, Kaia, Optimism, Polygon | [createWebhook.md](spec/createWebhook.md) |
| Create (Aptos) | Create a webhook for Aptos on-chain events | `aptos-createWebhook` | Aptos | [aptos-createWebhook.md](spec/aptos-createWebhook.md) |
| Get | Retrieve configuration and status of a registered webhook | `getWebhook` | Arbitrum, Base, BNB, Ethereum, Giwa, Kaia, Optimism, Polygon, Aptos | [getWebhook.md](spec/getWebhook.md) |
| Update | Modify webhook URL, filter conditions, and other settings | `updateWebhook` | Arbitrum, Base, BNB, Ethereum, Giwa, Kaia, Optimism, Polygon | [updateWebhook.md](spec/updateWebhook.md) |
| Update (Aptos) | Modify Aptos webhook settings | `aptos-updateWebhook` | Aptos | [aptos-updateWebhook.md](spec/aptos-updateWebhook.md) |
| Delete | Delete a registered webhook | `deleteWebhook` | Arbitrum, Base, BNB, Ethereum, Giwa, Kaia, Optimism, Polygon, Aptos | [deleteWebhook.md](spec/deleteWebhook.md) |
| History | Retrieve webhook delivery history and response status | `getWebhookHistory` | Arbitrum, Base, BNB, Ethereum, Giwa, Kaia, Optimism, Polygon, Aptos | [getWebhookHistory.md](spec/getWebhookHistory.md) |
