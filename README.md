# Chainsnap
[![Made by FogMeta](https://img.shields.io/badge/made%20by-FogMeta-green.svg)](https://fogmeta.com/)
[![Follow on Twitter](https://img.shields.io/badge/follow_on%20-Twitter-brightgreen.svg)](https://twitter.com/FogMeta)
[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg)](https://github.com/RichardLitt/standard-readme)

## Introduction
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

## Snapshots
 - [Filecoin Snapshots](Filecoin/README.md ':include')
 - [Polygon Snapshots](Polygon/README.md ':include')
 - [Pocket Snapshots](Pocket/README.md ':include')
 - [Binance Smart Chain Snapshots](Binance_Smart_Chain/README.md ':include')
 - [Ethereum Snapshots](Ethereum/README.md ':include')
 - [Aptos Snapshots](Aptos/README.md ':include')
 - [Near Snapshots](Near/README.md ':include')

## Backup Frequency
| Snapshot Name | Backup Frequency |
| --- | --- |
| Aptos | Weekly |
| Binance Smart Chain | Weekly |
| Ethereum | Monthly |
| Filecoin | Weekly |
| Near | Weekly |
| Pocket | Twice a week |
| Polygon | Weekly |
