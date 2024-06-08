---
description: Running a valid and updated BTQ (Bitcoin Quantum)
---

# BTQ Node Uses

Running a valid and updated BTQ (Bitcoin Quantum) node significantly contributes to the security and efficiency of the blockchain network. Here, we will explore the various functions and uses of a BTQ Node, expanding beyond the basics covered in previous documents.

## Security

At the heart of the BTQ blockchain lies a decentralized peer-to-peer network. This network achieves consensus on key aspects of the blockchain, such as block height, previous block header hash, transactions included in each block, and the mining rewards payout address. The overall security of the blockchain increases with the number of peers participating in this consensus process.

The threat of majority control by malicious actors, known as a 51% attack, can manipulate chain data and cause various blockchain exploits. The most effective defense against this threat is to increase the number of nodes, diluting the potential influence of any single malicious entity.

Additionally, running a node enhances the security of transactions made through it, ensuring they remain unaltered and are broadcast correctly to the legitimate network.

### Transaction Security

Transactions processed through a local, secure node are protected from tampering and are reliably broadcast to the active network, ensuring they are added to the correct version of the blockchain.

## Wallet Functions

A BTQ node plays a crucial role in broadcasting signed transactions to the network, ensuring they are added to a block that is validated and agreed upon by the network consensus. Transactions requiring a one-time signature (OTS) key for actions like sending BTQ, messaging, notarizing data, or creating tokens must be processed through a node. All BTQ wallet tools have the functionality to interact with a local node.

## Chain Analytics Functions

For accurate and uninterrupted data access, running a local node is advisable. This allows developers and users to access historical data and integrate new chain data seamlessly into their applications.

## Mining Functions

A full BTQ node can directly participate in mining using the computer's CPU, or facilitate pooled mining activities by coordinating multiple computers within a mining pool.

### Broadcasting Transactions

Every transaction sent to the network interacts with a node. For example, the wallet software signs a transaction with a private key, which is then transmitted via a BTQ node. The node checks the transaction for issues such as OTS key reuse—if the OTS key has already been used, the node rejects the transaction to prevent security risks.

### Chain Data Lookup

When querying an address balance or verifying a transaction, a BTQ node accesses the historical data stored in the blockchain. This data is maintained in the node’s state files, which are validated through a peer-to-peer syncing process and cryptographic verifications by network peers.

These functions highlight the critical role of BTQ nodes in maintaining the integrity, security, and functionality of the BTQ blockchain network.
