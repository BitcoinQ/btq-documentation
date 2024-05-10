---
description: >-
  Discover the core functionalities and operations of BTQ nodes on our detailed
  overview page.
---

# BTQ Node Overview

A BTQ node is a specialized computer that runs software developed by the BTQ team. These nodes are fundamental to the network's infrastructure, acting as the building blocks that strengthen the blockchain. Each node collaborates with others to achieve consensus on the blockchain's state, determining the next valid block in the chain.

Nodes play a crucial role in processing and incorporating transactions into the blockchain's history from the transaction mempool. This collective operation by various nodes across the network ensures a robust, decentralized agreement on each block, reinforcing the integrity and continuity of the distributed ledger. This is the essence of the BTQ blockchain, where each participating node helps to maintain the ledger's accuracy and security.

## BTQ Network

The Peer-To-Peer network formed by BTQ nodes provides the fundamental security that underpins the blockchain. Through sophisticated mathematical algorithms and an ultra-secure address scheme using post-quantum cryptography, BTQ has established one of the most secure and trusted blockchains in existence today.

Running a BTQ node is straightforward. To get started, refer to the installation documentation which will guide you through the setup process, ensuring you can contribute to the network's strength and participate actively in the BTQ ecosystem.

### Basic Functions of a BTQ Node

A BTQ node performs several critical functions that are essential for the maintenance and operation of the blockchain network:

1. **Validate Transactions**: Nodes ensure that all transactions meet the network's protocols and rules. This includes checking the validity of signatures and ensuring transactions do not double-spend.
2. **Mint New Blocks**: Nodes are responsible for creating new blocks. This involves selecting valid transactions from the mempool, forming them into a block, and solving the cryptographic puzzle necessary to add the block to the blockchain.
3. **Consensus on History**: Nodes work collaboratively to achieve consensus on a unified and immutable history of transactions. This process ensures that all copies of the distributed ledger are the same across the network.
4. **Provide Blockchain History**: Nodes make the blockchain's history accessible to anyone who wishes to validate past transactions or audit the ledger.
5. **API for Transactions**: Nodes provide an API that allows applications to interact with the blockchain. This includes sending transactions to the network and accessing information about the ledger.
   * **Sending Transactions**: Nodes receive transactions from users or applications and broadcast them to the network for validation and inclusion in the blockchain.
   * **Validating Funds in Wallets**: Nodes check the balance of addresses to confirm that they have sufficient funds to cover the transactions they are attempting to make.

These functionalities ensure that the BTQ blockchain remains secure, transparent, and accessible, allowing it to function effectively as a decentralized ledger.

### Broadcasting Transactions with a BTQ Node

When a transaction is sent to the BTQ network, it always interacts with a node, regardless of the source.

**How Transactions are Processed:**

1. **Transaction Initiation**: Users or applications, such as wallet software, initiate a transaction. The wallet uses a private key to sign the transaction, which is then forwarded to the network through a BTQ node managed by the foundation.
2. **Receiving Transactions**: The node listens for incoming transactions from users' wallet applications and takes the initial steps to process them.
3. **Verification Checks**: Before a transaction can enter the mempool (the collection of all transactions waiting to be confirmed and included in a block), the node performs several verification checks. These checks include:
   * **OTS Key Usage**: The node checks if the One-Time Signature (OTS) key used for signing the transaction has been previously used. If it has, the transaction is rejected to prevent the reuse of OTS keys, enhancing security against potential fraud.
   * **Fund Sufficiency**: The node verifies if the originating address has enough funds to cover the transaction fee and the amount being transferred. If not, the transaction is rejected.
4. **Broadcasting to Peers**: Once a transaction passes all checks, the node broadcasts it to other nodes in the network. This dissemination ensures that the transaction is added to the next available block, pending consensus from other nodes.

**Additional Information:**

* **OTS Key Documentation**: To understand more about how OTS keys work and why they must not be reused, users can refer to the OTS Key Documentation. This resource provides detailed insights into the security mechanisms embedded in the BTQ network through its use of post-quantum cryptographic methods.

In summary, every transaction broadcast through the BTQ network is carefully scrutinized by nodes to ensure it adheres to network rules and protocols. This process not only secures the network but also maintains the integrity and reliability of the blockchain.

### Chain Data Lookup in BTQ Network

**Overview** Chain data lookup is a critical process in the BTQ network that involves querying and verifying the history of addresses and transactions. This function ensures transparency and trust within the network by allowing any participant to access and verify transaction details.

**Process Details**

1. **Historical Data Access**: When an address balance is queried or a transaction is verified, the network looks up the historical data stored on the blockchain. This includes all past transactions linked to the specific address or the transaction details in question.
2. **Data Storage**: Transaction data and address histories are stored in the node's chain state files, which constitute a leveled database structure. This organization facilitates efficient data retrieval and management.
3. **Network Consensus**: All data on the blockchain, including transaction histories and address balances, has been validated and agreed upon by a majority of nodes in the network through the consensus process. This ensures that the data is accurate and reliable.
4. **Verification through P2P Syncing**: The peer-to-peer (P2P) syncing process is fundamental for maintaining the integrity of the blockchain. During this process, nodes continuously exchange data to keep their local copies of the blockchain updated and synchronized with the latest state of the ledger.
5. **Cryptographic Hash Verification**: To further validate transactions, nodes check cryptographic hashes provided by other peers in the network. These hashes serve as proofs of the transaction’s validity and integrity, ensuring that the data has not been altered.

**Importance of Chain Data Lookup**

* **Transparency**: Provides clear visibility into the transaction history and balances, crucial for trust and accountability in the network.
* **Security**: The use of cryptographic hashes and the consensus mechanism among nodes helps prevent fraud and unauthorized alterations of the blockchain.
* **Accessibility**: Enables participants to independently verify the legitimacy of transactions and the status of funds, which is essential for operational security and user confidence.

Through these mechanisms, the BTQ network maintains a secure, accurate, and transparent record of all transactions, ensuring that the blockchain remains a reliable and robust platform for digital transactions.
