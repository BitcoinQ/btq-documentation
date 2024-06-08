---
description: Here's the adapted guide for the BTQ Explorer Block Lookup
---

# BTQ Explorer Block Lookup

## BTQ Explorer Block Lookup

To lookup a block on the chain, simply enter the block number into the search bar at the top of the BTQ Explorer site.

This will return all relevant information from that block as found in the immutable blockchain. This information will be the same no matter which node is queried as the chain came to consensus when the block was minted.

### Block Information

At the top of the page will be general information about the block, when it was minted, and how many transactions are contained in the block. At least one transaction will be found for every block called a coinbase transaction, which is the payout to the miner that minted the block.

| Information  | Example Data      | Notes                                                       |
| ------------ | ----------------- | ----------------------------------------------------------- |
| Transactions | 2                 | The number of transactions contained in the block           |
| Timestamp    | 06:16 26 Jun 2018 | When the block was minted on the chain                      |
| Epoch        | 0                 | The epoch the block was made in, increases every 100 blocks |
| Size         | 2.976 KB          | The total size of the block                                 |
| Reward       | 6.656333953 BTQ   | Amount of BTQ given as a block reward to the miner          |
| Mining Nonce | 2781151944        | Nonce that was used for mining the block                    |

### Transactions

Below the block information will be a list of all transactions contained in the block queried. This information table is broken into multiple columns.

* **Type**: The type of transaction sent
* **Amount**: Amount of BTQ
* **Fee (Shor)**: Fee paid for the transaction
* **From**: From BTQ address
* **To**: To BTQ address
* **Txhash**: Transaction hash for the given transaction

### Meta Information

Below the table will be a dropdown that provides additional meta information related to the block and all of the transactions contained within.

This data is what the node returns and is used to provide the user-friendly information printed above.

This guide ensures you can effectively use the BTQ Block Explorer to look up and understand the details of BTQ blocks.
