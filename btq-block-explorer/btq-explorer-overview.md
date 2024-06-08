---
description: Here's the corrected and detailed guide for the BTQ Explorer
---

# BTQ Explorer Overview

## BTQ Explorer Overview

The Block Explorer is a portal into the BTQ blockchain, allowing users to lookup information directly from the chain.

The explorer is connected through a BTQ node, and the information provided is sourced from the immutable data contained in the blockchain. All transactions, addresses that have seen transactions, tokens, mining payouts, etc., are stored and accessible through the explorer.

**NOTE:** An address that has been generated but has not transacted on-chain, either received or transmitted, will not be found with the explorer. A transaction is required prior to being discoverable by the explorer.

More information can be found in the Address Documentation.

The main explorer page can be accessed through any modern web browser and is located at [https://explorer.bitcoinq.xyz](https://explorer.bitcoinq.xyz).

From the main page, there are links along the sidebar for all of the various functions of the tool. These link to additional functionality that expands on the main page info.

* **Blocks**: Shows the latest blocks minted onto the chain.
* **Recent Transactions**: Shows a list of the latest transactions shown on the chain.
* **Unconfirmed Transactions**: Shows any transactions that are in the Mempool awaiting a block to mint.
* **Peers**: Gives a list of all peers the explorer node is aware of.
* **Richlist**: Full list of all public addresses ranked in total value.
* **Wallet**: This is a link to the BTQ Web Wallet.

## Network Status

This section gives overall information on the network and is pulled directly from the BTQ node that the explorer is using. This helps to verify that the node is synced and up to date, ensuring correct blockchain information is provided.

* **Connected Status**: This gives confirmation that the node is connected to other peers and is working to secure and further the chain.
  * Example status: `Connected: SYNCED`
* **Uptime**: This gives the connected explorer node's uptime, or how long the node has been connected and functioning on the chain.
  * Example status: `Uptime: 30d 1h 44min`
* **Network Code Name**: This section gives information on the chain connected to using the chain's code name. For MainNet, this will be "Mainnet," the code name given to the chain at the time of genesis, or the launch of the chain.
  * Example status: `Mainnet`
  * **INFO**: TestNet will have a different code name, and this will change each time the test network is restarted. Ensure you are looking at the correct chain information!
* **Active Peers**: This section prints the number of active peers that are connected to the explorer node. This is not necessarily the total number of peers connected on the entire chain due to how Peer-To-Peer networks function.
  * Example status: `Explorer node active peers: 63`
* **Version**: This information refers to the version of core code that the node is running. This can be found in the core code repository located in BTQ's GitHub.
  * Example status: `Version: 4.0.0 python`
  * **INFO**: At the time of writing, the latest version is 4.0.0

## Blocks

The blocks section covers information on the connected node related to blocks found in the chain. These blocks contain all transactions minted in that block, as well as the mining reward that is paid to the miner who minted the block.

* **Max Index**: The max index section shows the current block height as seen by the connected node. If the Connected status is SYNCED, this will be the agreed and coordinated block height of all connected nodes, and the latest block of the chain.
  * Example status: `Max Index: 2579678`
  * **INFO**: If you are syncing a local node, this number should match once your node is fully synced.
* **Block Time**: This gives the last time between minting new blocks, or the time taken to mine and agree on consensus of the chain by all nodes. This time may fluctuate a little depending on network traffic and the amount of mining hashrate seen on the network.
  * Example status: `Block Time: 58`
* **Block Time Std Dev**: This shows the standard variation of block time between blocks.
  * Example status: `Block Time Std Dev: 64`
* **Coin Supply**: This section shows general information on the emissions of the block rewards and total amount of coins mined and to be mined.
  * **Emission**: This is the percentage of total coin supply that has been distributed, and the total number of BTQ in circulation.
    * Example status: `Emission: 32% (3,200,307.48)`
  * **Unmined**: This shows the total supply that is yet to be mined and distributed in block rewards. These BTQ will be distributed over the exponential decay curve over the next estimated 1000 years, a 5% reduction in block rewards every 525,600 blocks.
    * Example status: `Unmined: 17,799,692.52`
  * **Block Reward**: This is the current block reward that is distributed to the miner who mints the next block. This number will continue to diminish according to the emission algorithm.
    * Example status: `Block Reward: 1.733252118`

## Hash Graph

The graph shows various information on the mining status and difficulty of the chain. This information changes depending on a few different conditions such as the network hashrate, connected miners, and recent changes to the hashrate that affect the difficulty of mining operations.

## Latest Blocks

This section shows the latest blocks that have been mined. You can select a block by clicking on it to delve into the details for that block.

**INFO**: See the Block Lookup documentation for more information.

## Latest Transactions

The latest transactions section shows any transactions that have shown up in the mempool since the last block was mined, as well as some of the most

This guide ensures you can effectively use the BTQ Block Explorer to interact with and monitor the BTQ blockchain.
