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
| complete_chain_with_finality_stateroots_2205870_2022-09-29_20-15-00.car | [2022-09-29](https://fil-chain-snapshots-fallback.s3.amazonaws.com/mainnet/complete_chain_with_finality_stateroots_2205870_2022-09-29_20-15-00.car)| [CSV]( Filecoin/complete_chain_with_finality_stateroots_2205870_2022-09-29_20-15-00.car.csv ':include') <br> [JSON]( Filecoin/complete_chain_with_finality_stateroots_2205870_2022-09-29_20-15-00.car.json ':include')  |[swan-task-fl9rov-auto-deals.json](Filecoin/swan-task-fl9rov-auto-deals.json ':include') <br> [swan-task-p9dh7u-auto-deals.json](Filecoin/swan-task-p9dh7u-auto-deals.json ':include') | [fl9rov.nft](https://opensea.io/assets/matic/0xA6787587159c017AD83fe28e746FCFAE0DD91383/43) <br>  [p9dh7u.nft](https://opensea.io/assets/matic/0xA6787587159c017AD83fe28e746FCFAE0DD91383/42) |                       
| minimal_finality_stateroots_2287441_2022-10-28_04-00-30.car | [2022-10-28](https://fil-chain-snapshots-fallback.s3.amazonaws.com/mainnet/minimal_finality_stateroots_2287441_2022-10-28_04-00-30.car) | [CSV](Filecoin/minimal_finality_stateroots_2287441_2022-10-28_04-00-30.car.csv ':include') <br> [JSON](Filecoin/minimal_finality_stateroots_2287441_2022-10-28_04-00-30.car.json ':include') | [swan-task-fl9rov-auto-deals.json](Filecoin/swan-task-fl9rov-auto-deals.json ':include') <br> [swan-task-p9dh7u-auto-deals.json](Filecoin/swan-task-p9dh7u-auto-deals.json ':include')| [fl9rov.nft](https://opensea.io/assets/matic/0xA6787587159c017AD83fe28e746FCFAE0DD91383/43) <br> [p9dh7u.nft](https://opensea.io/assets/matic/0xA6787587159c017AD83fe28e746FCFAE0DD91383/42) |

#### 2. Polygon

| Network | Snapshot Name | Download Url | Snapshot Metadata | Deal Metadata | Deal Metadata NFT(opensea) |
| :-: | :-: | :-: | :-: | :-: | :-: |
| Erigon Mainnet | erigon-archive-snapshot-2022-10-12.tar.gz | [2022-10-12](https://matic-blockchain-snapshots.s3-accelerate.amazonaws.com/matic-mainnet/erigon-archive-snapshot-2022-10-12.tar.gz )| [CSV]( Polygon/erigon-archive-snapshot-2022-10-12.tar.gz.csv ':include') <br> [JSON]( Polygon/erigon-archive-snapshot-2022-10-12.tar.gz.json ':include')                 |               |                            |
|                                                              |                                                              |                   |               |                            |
