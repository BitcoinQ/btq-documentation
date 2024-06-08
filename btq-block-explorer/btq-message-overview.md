---
description: Here's the adapted guide for the BTQ Message Overview
---

# BTQ Message Overview

## BTQ Message Overview

The BTQ network supports on-chain messages providing a variety of functionality to the project. These messages are sent onto the BTQ network, writing data into the immutable quantum-resistant blockchain ledger.

Anyone is able to write data to the chain and can do so in multiple ways:

* **Transfer\_TX**: This message data is written during a transfer of funds. Most wallet software supports the addition of message data during a transfer of funds.
* **Message\_TX**: A dedicated message transaction where only the message data is transferred. Check the tools section of the BTQ Wallet software.

Messages can be retrieved by any user by simply searching for the block number that the message was added to or by searching the transaction hash using the BTQ block explorer.

**INFO:** Messages are limited to 80 bytes or 80 text characters that may be sent onto the BTQ blockchain. This limitation ensures blocks stay small in size.

### Transfer Transaction Message

During a typical transaction, where a user sends funds to another address, there is an additional and optional field that allows some message data to be inserted.

The use of this field is entirely up to the end user. For instance, it can be a simple text sentence that gives reference to the transaction for later, such as "Alice's weekly pay".

It may also be used to reference a transaction ID for some automated system to verify a user has sent funds, say in a point of sale payment system. The merchant could use this field to enter a unique transaction ID, then verify the funds were transferred into the merchant's address with a matching tx\_id prior to releasing a product to the customer.

The only limitation is the length of text (80 bytes or characters), and the user's imagination. Message data can be seen in the BTQ Explorer by referencing the transaction hash from the outgoing funds transfer.

### Message Transaction

This functionality has many uses and is the basis of a few other tools implemented on the BTQ chain, like the on-chain notarization functions.

At its core, the message is simply a string of text, established by the user sending the transaction. This string is limited to 80 bytes or text characters and will fail if anything larger than that is used.

**INFO:** To differentiate between established message types that have been implemented, the BTQ developers have established a standard message transaction encoding that allows a system to tell that the message is intended for processing. These systems then watch for this encoding and react accordingly.

The established message transaction encoding standard can be found at the BTQ GitHub repository and is hosted open source.

If you would like to add a new encoding to support a project you are working on, submit a PR to that repo following the standard set there.

This guide ensures you can effectively use the message functionality within the BTQ network for various purposes.
