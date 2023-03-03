# Chainsnap
### Introduction
Chainsnap is a project for maintaining blockchain snapshots. This project enables the storing and retrieval of snapshots for blockchain projects including Filecoin, Polygon, Ethereum, Binance Smart Chain, and Near.

**Main Features:**

  - Full backup of the completed and minimal snapshots (if it exists) of each chain every once in a while
 
  - Maintain the original download links of the snapshots and the metadata (CSV and JSON format) after preprocessing.
  - Each piece will be sent to storage providers in the Filecoin network through [Swan Client](https://github.com/filswan/go-swan-client), and the metadata of the deal (including filename, dealCID, MinerID, etc.) will be maintained in the repository;
  - Mint deal metadata to an NFT in the [Opensea platform](https://opensea.io/), everyone can see it at any time

**How to retrieve it:**
  - Get all pieces of each snapshot from snapshot metadata
  - Get storage providers that store all pieces from the deal metadata
  - Fetch all the pieces using the [Lotus retrieval function](https://lotus.filecoin.io/tutorials/lotus/store-and-retrieve/retrieve-data/#send-a-retrieval-request)
  - Merge all pieces to the complete snapshot

It is worth noting that all deal metadata will be mint to the Opensea platform through [multichain storage](https://www.multichain.storage/) to ensure that will never be lost


#### 1. Filecoin

| Snapshot Name | Download Url | Snapshot Metadata | Deal Metadata | Deal Metadata NFT(opensea) |
| :-: | :-: | :-: | :-: | :-: |
| complete_chain_with_finality_stateroots_2205870_2022-09-29_20-15-00.car | [2022-09-29](https://fil-chain-snapshots-fallback.s3.amazonaws.com/mainnet/complete_chain_with_finality_stateroots_2205870_2022-09-29_20-15-00.car)| [CSV]( Filecoin/2022-09-29_complete_chain/complete_chain_with_finality_stateroots_2205870_2022-09-29_20-15-00.car.csv ':include') <br> [JSON]( Filecoin/2022-09-29_complete_chain/complete_chain_with_finality_stateroots_2205870_2022-09-29_20-15-00.car.json ':include')  |[swan-task-fl9rov-auto-deals.json](Filecoin/2022-09-29_complete_chain/swan-task-fl9rov-auto-deals.json ':include') <br> [swan-task-p9dh7u-auto-deals.json](Filecoin/2022-09-29_complete_chain/swan-task-p9dh7u-auto-deals.json ':include') | [fl9rov.nft](https://opensea.io/assets/matic/0xA6787587159c017AD83fe28e746FCFAE0DD91383/43) <br>  [p9dh7u.nft](https://opensea.io/assets/matic/0xA6787587159c017AD83fe28e746FCFAE0DD91383/42) |                       
| minimal_finality_stateroots_2287441_2022-10-28_04-00-30.car | [2022-10-28](https://fil-chain-snapshots-fallback.s3.amazonaws.com/mainnet/minimal_finality_stateroots_2287441_2022-10-28_04-00-30.car) | [CSV](Filecoin/2022-10-28_minimal_chain/minimal_finality_stateroots_2287441_2022-10-28_04-00-30.car.csv ':include') <br> [JSON](Filecoin/2022-10-28_minimal_chain/minimal_finality_stateroots_2287441_2022-10-28_04-00-30.car.json ':include') | [swan-task-fl9rov-auto-deals.json](Filecoin/2022-09-29_complete_chain/swan-task-fl9rov-auto-deals.json ':include') <br> [swan-task-p9dh7u-auto-deals.json](Filecoin/2022-09-29_complete_chain/swan-task-p9dh7u-auto-deals.json ':include')| [fl9rov.nft](https://opensea.io/assets/matic/0xA6787587159c017AD83fe28e746FCFAE0DD91383/43) <br> [p9dh7u.nft](https://opensea.io/assets/matic/0xA6787587159c017AD83fe28e746FCFAE0DD91383/42) |
| datastore_chain_2023-02-02 | 2023-02-02(Local chain data) | [JSON-1](Filecoin/2023-02-02_datastore_chain/filecoin-snapshot-20230202-1.json ':include') <br> [JSON-2](Filecoin/2023-02-02_datastore_chain/filecoin-snapshot-20230202-2.json ':include') | [swan-task-giv8d5-metadata.json](Filecoin/2023-02-02_datastore_chain/swan-task-giv8d5-metadata.json ':include') <br> [swan-task-p9dh7u-auto-deals.json](Filecoin/2023-02-02_datastore_chain/swan-task-nymir7-metadata.json ':include')|  |
| datastore_chain_2023-02-09 | 2023-02-09(Local chain data) | [JSON](Filecoin/2023-02-09_datastore_chain/filecoin_chain-20230209.json ':include') | [swan-task-ea9sum-metadata.json](Filecoin/2023-02-09_datastore_chain/swan-task-ea9sum-metadata.json ':include') |  |
| datastore_chain_2023-02-15 | 2023-02-15(Local chain data) | [JSON](Filecoin/2023-02-15_datastore_chain/filecoin-chain-2023-02-15.json ':include') | [swan-task-2m5tt7-metadata.json](Filecoin/2023-02-15_datastore_chain/swan-task-2m5tt7-metadata.json ':include') |  |
| datastore_chain_2023-02-20 | 2023-02-20(Local chain data) | [JSON](Filecoin/2023-02-20_datastore_chain/datastore-2023-02-20.json ':include') | [swan-task-gx1u5r-metadata.json](Filecoin/2023-02-20_datastore_chain/swan-task-gx1u5r-metadata.json ':include') <br> [swan-task-hon1x0-metadata.json](Filecoin/2023-02-20_datastore_chain/swan-task-hon1x0-metadata.json ':include') <br> [swan-task-n6w7m2-metadata.json](Filecoin/2023-02-20_datastore_chain/swan-task-n6w7m2-metadata.json ':include')|  |

#### 2. Polygon

| Network | Snapshot Name | Download Url | Snapshot Metadata | Deal Metadata | Deal Metadata NFT(opensea) |
| :-: | :-: | :-: | :-: | :-: | :-: |
| Erigon Mainnet | erigon-archive-snapshot-2022-10-12.tar.gz | [2022-10-12](https://matic-blockchain-snapshots.s3-accelerate.amazonaws.com/matic-mainnet/erigon-archive-snapshot-2022-10-12.tar.gz )| [CSV]( Polygon/2022-10-12_erigon_archive/erigon-archive-snapshot-2022-10-12.tar.gz.csv ':include') <br> [JSON]( Polygon/2022-10-12_erigon_archive/erigon-archive-snapshot-2022-10-12.tar.gz.json ':include') | [erigon-archive-snapshot-2022-10-12.tar.gz.csv](Polygon/2022-10-12_erigon_archive/swan-task-lmrukl-auto-deals.json ':include')  <br> [swan-task-q1idna-auto-deals.json](Polygon/2022-10-12_erigon_archive/swan-task-q1idna-auto-deals.json ':include') |[q1idna.nft](https://opensea.io/assets/matic/0xA6787587159c017AD83fe28e746FCFAE0DD91383/51) <br> [lmrukl.nft](https://opensea.io/assets/matic/0xA6787587159c017AD83fe28e746FCFAE0DD91383/52) |
| Erigon Mainnet | erigon-archive-snapshot-2023-01-24.tar.gz | [2023-01-24](https://matic-blockchain-snapshots.s3-accelerate.amazonaws.com/matic-mainnet/erigon-archive-snapshot-2023-01-24.tar.gz )| [JSON-1]( Polygon/2023-01-24_erigon_archive/erigon-archive-2023-01-24-1.json ':include') <br> [JSON-2]( Polygon/2023-01-24_erigon_archive/erigon-archive-2023-01-24-2.json ':include') | [swan-task-hjw6fg-metadata.json](Polygon/2023-01-24_erigon_archive/swan-task-hjw6fg-metadata.json ':include')  <br> [swan-task-vlgigt-metadata.json](Polygon/2023-01-24_erigon_archive/swan-task-vlgigt-metadata.json ':include') <br> [erigon-archive-2023-01-24-1-metadata.json](Polygon/2023-01-24_erigon_archive/erigon-archive-2023-01-24-1-metadata.json ':include') <br> [erigon-archive-2023-01-24-2-metadata.json](Polygon/2023-01-24_erigon_archive/erigon-archive-2023-01-24-2-metadata.json ':include')|
| Bor Mainnet Fullnode | bor-fullnode-2023-01-24.tar.gz | [2023-01-24](https://matic-blockchain-snapshots.s3-accelerate.amazonaws.com/matic-mainnet/bor-fullnode-snapshot-2023-01-24.tar.gz )| [JSON-1](Polygon/2023-01-24_bor_fullnode/bor-fullnode-2023-01-24-1.json ':include') <br> [JSON-2](Polygon/2023-01-24_bor_fullnode/bor-fullnode-2023-01-24-2.json ':include') | [swan-task-7ynxiw-metadata.json](Polygon/2023-01-24_bor_fullnode/swan-task-7ynxiw-metadata.json ':include')  <br> [swan-task-mbwu1j-metadata.json](Polygon/2023-01-24_bor_fullnode/swan-task-mbwu1j-metadata.json ':include') <br> [bor-fullnode-2023-01-24-1-metadata.json](Polygon/2023-01-24_bor_fullnode/bor-fullnode-2023-01-24-1-metadata.json ':include') <br> [bor-fullnode-2023-01-24-2-metadata.json](Polygon/2023-01-24_bor_fullnode/bor-fullnode-2023-01-24-2-metadata.json ':include') |
| Heimdall Mainnet | heimdall-snapshot-2023-01-25.tar.gz | [2023-01-25](https://matic-blockchain-snapshots.s3-accelerate.amazonaws.com/matic-mainnet/heimdall-snapshot-2023-01-25.tar.gz )| [JSON-1]( Polygon/2023-01-25_heimdall/heimdall-2023-01-25-1.json ':include') <br> [JSON-2]( Polygon/2023-01-25_heimdall/heimdall-2023-01-25-2.json ':include')  | [swan-task-qywbkd-metadata.json](Polygon/2023-01-25_heimdall/swan-task-qywbkd-metadata.json ':include')  <br> [swan-task-z2rxty-metadata.json](Polygon/2023-01-25_heimdall/swan-task-z2rxty-metadata.json ':include') <br> [swan-task-rroxyp-metadata.json](Polygon/2023-01-25_heimdall/swan-task-rroxyp-metadata.json ':include') <br> [heimdall-2023-01-25-1-metadata.json](Polygon/2023-01-25_heimdall/heimdall-2023-01-25-1-metadata.json ':include') <br> [heimdall-2023-01-25-2-metadata.json](Polygon/2023-01-25_heimdall/heimdall-2023-01-25-2-metadata.json ':include') | |
| Erigon Mumbai Archive | erigon-mumbai-archive-2023-01-30.tar.gz | [2023-01-30](https://matic-blockchain-snapshots.s3-accelerate.amazonaws.com/matic-mainnet/erigon-mumbai-archive-2023-01-30.tar.gz )| [JSON-1]( Polygon/2023-01-25_heimdall/heimdall-2023-01-25-1.json ':include') <br> [JSON-2]( Polygon/2023-01-30_erigon_mumbai_archive/erigon-mumbai-archive-2023-01-30-2.json ':include') | [swan-task-5lh53i-metadata.json](Polygon/2023-01-30_erigon_mumbai_archive/swan-task-5lh53i-metadata.json ':include')  <br> [swan-task-k0oban-metadata.json](Polygon/2023-01-30_erigon_mumbai_archive/swan-task-k0oban-metadata.json ':include') <br> [erigon-mumbai-archive-2023-01-30-1-metadata.json](Polygon/2023-01-30_erigon_mumbai_archive/erigon-mumbai-archive-2023-01-30-1-metadata.json ':include') <br> [erigon-mumbai-archive-2023-01-30-2-metadata.json](Polygon/2023-01-30_erigon_mumbai_archive/erigon-mumbai-archive-2023-01-30-2-metadata.json ':include') | |
| Heimdall | heimdall-2023-02-06.tar.gz | [2023-02-06](https://matic-blockchain-snapshots.s3-accelerate.amazonaws.com/matic-mainnet/heimdall-2023-02-06.tar.gz )| [JSON-1]( Polygon/2023-02-06_heimdall/heimdall-2023-02-06-1.json ':include') <br> [JSON-2]( Polygon/2023-02-06_heimdall/heimdall-2023-02-06-2.json ':include') | [swan-task-4zvphi-metadata.json](Polygon/2023-02-06_heimdall/swan-task-4zvphi-metadata.json ':include')  <br> [swan-task-fxnjl6-metadata.json](Polygon/2023-02-06_heimdall/swan-task-fxnjl6-metadata.json ':include') <br> [heimdall-2023-02-06-1-metadata.json](Polygon/2023-02-06_heimdall/heimdall-2023-02-06-1-metadata.json ':include') <br> [heimdall-2023-02-06-2-metadata.json](Polygon/2023-02-06_heimdall/heimdall-2023-02-06-2-metadata.json ':include')| |
| Bor Fullnode | bor-fullnode-2023-02-07.tar.gz | [2023-02-07](https://matic-blockchain-snapshots.s3-accelerate.amazonaws.com/matic-mainnet/bor-fullnode-2023-02-07.tar.gz )| [JSON-1](Polygon/2023-02-07_bor_fullnode/bor-fullnode-2023-02-07-1.json ':include') <br> [JSON-2](Polygon/2023-02-07_bor_fullnode/bor-fullnode-2023-02-07-2.json ':include') | [swan-task-0php4a-metadata.json](Polygon/2023-02-07_bor_fullnode/swan-task-0php4a-metadata.json ':include')  <br> [swan-task-xdlzu1-metadata.json](Polygon/2023-02-07_bor_fullnode/swan-task-xdlzu1-metadata.json ':include') <br> [bor-fullnode-2023-02-07-1-metadata.json](Polygon/2023-02-07_bor_fullnode/bor-fullnode-2023-02-07-1-metadata.json ':include') <br> [bor-fullnode-2023-02-07-2-metadata.json](Polygon/2023-02-07_bor_fullnode/bor-fullnode-2023-02-07-2-metadata.json ':include') |
| Bor Fullnode | bor-fullnode-2023-02-09.tar.gz | [2023-02-09](https://matic-blockchain-snapshots.s3-accelerate.amazonaws.com/matic-mainnet/bor-fullnode-2023-02-09.tar.gz )| [JSON-1](Polygon/2023-02-09_bor_fullnode/bor-fullnode-2023-02-09-1.json ':include') <br> [JSON-2](Polygon/2023-02-09_bor_fullnode/bor-fullnode-2023-02-09-2.json ':include') | [swan-task-bb5lvg-metadata.json](Polygon/2023-02-09_bor_fullnode/swan-task-bb5lvg-metadata.json ':include')  <br> [swan-task-c7m7pq-metadata.json](Polygon/2023-02-09_bor_fullnode/swan-task-c7m7pq-metadata.json ':include') <br> [bor-fullnode-2023-02-09-1-metadata.json](Polygon/2023-02-09_bor_fullnode/bor-fullnode-2023-02-09-1-metadata.json ':include') <br> [bor-fullnode-2023-02-09-2-metadata.json](Polygon/2023-02-09_bor_fullnode/bor-fullnode-2023-02-09-2-metadata.json ':include') |

#### 3. Pocket

| Network | Snapshot Name | Download Url | Snapshot Metadata | Deal Metadata | Deal Metadata NFT(opensea) |
| :-: | :-: | :-: | :-: | :-: | :-: |
| Pocket Mainnet | pocket-74617.tar | [2023-02-03](https://snapshot.nodes.pokt.network/latest.tar )| [JSON-1]( Pocket/2023-02-03_74617/pocket-snapshot-74617-20230203-1.json ':include') <br> [JSON-2]( Pocket/2023-02-03_74617/pocket-snapshot-74617-20230203-1.json ':include') | [swan-task-l1z54s-metadata.json](Pocket/2023-02-03_74617/swan-task-l1z54s-metadata.json ':include')  <br> [swan-task-qau6h8-metadata.json](Pocket/2023-02-03_74617/swan-task-qau6h8-metadata.json ':include') | |
| Pocket Mainnet | pocket.tar | [2023-02-15](https://snapshot.nodes.pokt.network/latest.tar )| [JSON]( Pocket/2023-02-03_74617/pocket-snapshot-74617-20230203-1.json ':include') | [swan-task-ua7zz9-auto-deals.csv](Pocket/2023-02-15/swan-task-ua7zz9-auto-deals.csv ':include') <br> [swan-task-ua7zz9-auto-deals.json](Pocket/2023-02-03_74617/swan-task-l1z54s-metadata.json ':include') | |

#### 4. Binance Smart Chain

| Snapshot Name | Download Url | Snapshot Metadata | Deal Metadata | Deal Metadata NFT(opensea) |
| :-: | :-: | :-: | :-: | :-: |
| BSC-snap.tar.gz | [2023-02-20](https://binance-smart-chain-snapshot.s3.amazonaws.com/snap.tar.gz)| [JSON]( Binance_Smart_Chain/2023-02-20_bsc/bsc-2023-02-20.json ':include') | [swan-task-ilmyi2-auto-deals.json](Binance_Smart_Chain/2023-02-20_bsc/swan-task-ilmyi2-auto-deals.json ':include') | |

#### 5. Ethereum

| Snapshot Name | Download Url | Snapshot Metadata | Deal Metadata | Deal Metadata NFT(opensea) |
| :-: | :-: | :-: | :-: | :-: |
| ETH_2023-02-21 | [2023-02-21](s3://public-blockchain-snapshots/eth/)| [CSV]( Ethereum/2023-02-21_eth_datastore/eth-2023-02-21.csv ':include') | [swan-task-bx4loj-auto-deals.json](Ethereum/2023-02-21_eth_datastore/swan-task-bx4loj-auto-deals.json ':include') | |

#### 6. Aptos

| Network | Snapshot Name | Download Url | Snapshot Metadata | Deal Metadata | Deal Metadata NFT(opensea) |
| :-: | :-: | :-: | :-: | :-: | :-: |
| Aptos Mainnet | aptos20230215.tar.lz4 | [2023-02-15](https://snapshots.bwarelabs.com/aptos/mainnet/aptos20230215.tar.lz4 )| [JSON]( Aptos/2023-02-15_apt_mainnet/aptos_mainnet-2023-02-15.json ':include') | [swan-task-aptos_mainnet-2023-02-15-metadata.json](Aptos/2023-02-15_apt_mainnet/swan-task-aptos_mainnet-2023-02-15-metadata.json ':include') | |
| Aptos Testnet | aptos20230215.tar.lz4 | [2023-02-15](https://snapshots.bwarelabs.com/aptos/testnet/aptos20230215.tar.lz4 )| [JSON]( Aptos/2023-02-15_apt_testnet/aptos_testnet-2023-02-15.json ':include') | [swan-task-aptos_testnet-2023-02-15-metadata.json](Aptos/2023-02-15_apt_testnet/swan-task-aptos_testnet-2023-02-15-metadata.json ':include') | |
| Aptos Mainnet | aptos20230221.tar.lz4 | [2023-02-21](https://snapshots.bwarelabs.com/aptos/mainnet/aptos20230221.tar.lz4 )| [JSON]( Aptos/2023-02-21_apt_mainnet/aptos_mainnet-2023-02-21.json ':include') | [swan-task-aptos_mainnet-2023-02-21-metadata.json](Aptos/2023-02-21_apt_mainnet/swan-task-aptos_mainnet-2023-02-21-metadata.json ':include') | |
| Aptos Testnet | aptos20230221.tar.lz4 | [2023-02-21](https://snapshots.bwarelabs.com/aptos/testnet/aptos20230221.tar.lz4 )| [JSON]( Aptos/2023-02-21_apt_testnet/aptos_testnet-2023-02-21.json ':include') | [swan-task-aptos_testnet-2023-02-21-metadata.json](Aptos/2023-02-21_apt_testnet/swan-task-aptos_testnet-2023-02-21-metadata.json ':include') | |
| Aptos Mainnet | aptos20230224.tar.lz4 | [2023-02-24](https://snapshots.bwarelabs.com/aptos/mainnet/aptos20230224.tar.lz4 )| [JSON]( Aptos/2023-02-24_apt_mainnet/aptos_mainnet-2023-02-24.json ':include') | [swan-task-aptos_mainnet-2023-02-24-metadata.json](Aptos/2023-02-24_apt_mainnet/swan-task-aptos_mainnet-2023-02-24-metadata.json ':include') | |
| Aptos Testnet | aptos20230224.tar.lz4 | [2023-02-24](https://snapshots.bwarelabs.com/aptos/testnet/aptos20230224.tar.lz4 )| [JSON]( Aptos/2023-02-24_apt_testnet/aptos_testnet-2023-02-24.json ':include') | [swan-task-aptos_testnet-2023-02-24-metadata.json](Aptos/2023-02-24_apt_testnet/swan-task-aptos_testnet-2023-02-24-metadata.json ':include') | |
| Aptos Mainnet | aptos20230225.tar.lz4 | [2023-02-25](https://snapshots.bwarelabs.com/aptos/mainnet/aptos20230225.tar.lz4 )| [JSON]( Aptos/2023-02-25_apt_mainnet/aptos_mainnet-2023-02-25.json ':include') | [swan-task-aptos_mainnet-2023-02-25-metadata.json](Aptos/2023-02-25_apt_mainnet/swan-task-aptos_mainnet-2023-02-25-metadata.json ':include') | |
| Aptos Testnet | aptos20230225.tar.lz4 | [2023-02-25](https://snapshots.bwarelabs.com/aptos/testnet/aptos20230225.tar.lz4 )| [JSON]( Aptos/2023-02-25_apt_testnet/aptos_testnet-2023-02-25.json ':include') | [swan-task-aptos_testnet-2023-02-25-metadata.json](Aptos/2023-02-25_apt_testnet/swan-task-aptos_testnet-2023-02-25-metadata.json ':include') | |
| Aptos Mainnet | aptos20230226.tar.lz4 | [2023-02-26](https://snapshots.bwarelabs.com/aptos/mainnet/aptos20230226.tar.lz4 )| [JSON]( Aptos/2023-02-26_apt_mainnet/aptos_mainnet-2023-02-26.json ':include') | [swan-task-aptos_mainnet-2023-02-26-metadata.json](Aptos/2023-02-26_apt_mainnet/swan-task-aptos_mainnet-2023-02-26-metadata.json ':include') | |
| Aptos Testnet | aptos20230226.tar.lz4 | [2023-02-26](https://snapshots.bwarelabs.com/aptos/testnet/aptos20230226.tar.lz4 )| [JSON]( Aptos/2023-02-26_apt_testnet/aptos_testnet-2023-02-26.json ':include') | [swan-task-aptos_testnet-2023-02-26-metadata.json](Aptos/2023-02-26_apt_testnet/swan-task-aptos_testnet-2023-02-26-metadata.json ':include') | |
| Aptos Mainnet | aptos20230227.tar.lz4 | [2023-02-27](https://snapshots.bwarelabs.com/aptos/mainnet/aptos20230227.tar.lz4 )| [JSON]( Aptos/2023-02-27_apt_mainnet/aptos_mainnet-2023-02-27.json ':include') | [swan-task-aptos_mainnet-2023-02-27-metadata.json](Aptos/2023-02-27_apt_mainnet/swan-task-aptos_mainnet-2023-02-27-metadata.json ':include') | |
| Aptos Testnet | aptos20230227.tar.lz4 | [2023-02-27](https://snapshots.bwarelabs.com/aptos/testnet/aptos20230227.tar.lz4 )| [JSON]( Aptos/2023-02-27_apt_testnet/aptos_testnet-2023-02-27.json ':include') | [swan-task-aptos_testnet-2023-02-27-metadata.json](Aptos/2023-02-27_apt_testnet/swan-task-aptos_testnet-2023-02-27-metadata.json ':include') | |
| Aptos Mainnet | aptos20230228.tar.lz4 | [2023-02-28](https://snapshots.bwarelabs.com/aptos/mainnet/aptos20230228.tar.lz4 )| [JSON]( Aptos/2023-02-28_apt_mainnet/aptos_mainnet-2023-02-28.json ':include') | [swan-task-aptos_mainnet-2023-02-28-metadata.json](Aptos/2023-02-28_apt_mainnet/swan-task-aptos_mainnet-2023-02-28-metadata.json ':include') | |
| Aptos Testnet | aptos20230228.tar.lz4 | [2023-02-28](https://snapshots.bwarelabs.com/aptos/testnet/aptos20230228.tar.lz4 )| [JSON]( Aptos/2023-02-28_apt_testnet/aptos_testnet-2023-02-28.json ':include') | [swan-task-aptos_testnet-2023-02-28-metadata.json](Aptos/2023-02-28_apt_testnet/swan-task-aptos_testnet-2023-02-28-metadata.json ':include') | |
