---
description: Maintaining a BTQ (Bitcoin Quantum) node
---

# BTQ Node Maintenance

Maintaining a BTQ (Bitcoin Quantum) node requires minimal effort, but there are several considerations to ensure its smooth operation over time.

## State File Growth

Like any blockchain, the BTQ chain grows with each new block added. This growth is crucial for achieving immutability, as it preserves the entire history of transactions for verification.

On average, the BTQ blockchain grows by about 2.95KB per block, with an average block time of around 60 seconds. As of the latest update, the blockchain requires approximately 10GB of space.

**Note:** It's important to plan for future growth; if the disk becomes full, the node will stop syncing new blocks. Currently, the blockchain occupies about 10GB of space at blockheight 1889766.

## BTQ Log

Node operations are logged in a file, typically located at `~/.btq/btq.log`. This log file rolls over into a backup once it reaches 100MB. These log files can accumulate, potentially using significant disk space, so monitoring them is advisable.

## Periodic Updates

Throughout the life of BTQ, the node software will require updates and upgrades:

### **Soft Fork**

A soft fork is an update that introduces new features or bug fixes while maintaining backward compatibility with older versions of the software. This means nodes running both old and new software can coexist on the same network. Soft forks do not require all node operators to update, and they generally affect only a subset of users.

### **Hard Fork**

A hard fork introduces significant changes that require all nodes to update to the latest software version. Failure to update by the specified blockheight results in the creation of two separate networks: one running the outdated software and another running the latest version. Nodes on the old software will not be recognized by the main network post-fork.

**Info:** Hard fork updates are announced well in advance of the fork height. It's recommended to join the BTQ mailing list or the support chat on platforms like Discord to stay informed about updates.

These maintenance tips will help ensure that your BTQ node operates efficiently and remains in sync with the network's latest standards and practices.
