---
description: The BTQ Web Wallet
---

# Overview BTQ Web Wallet

The BTQ Web Wallet offers the most straightforward interface for interacting with your BTQ wallet. It can be accessed at [https://wallet.bitcoinq.xyz](https://wallet.bitcoinq.xyz), where users can create new addresses, transact on the network, and access a variety of on-chain tools.

## Note

All secure cryptographic operations in the BTQ Web Wallet are executed locally in your browser or desktop application through a WebAssembly-compiled version of the BTQ library. The private keys remain within the memory space of the wallet application and are automatically erased the moment the browser window is closed.

## General Info

BTQ, being a quantum-resistant blockchain, utilizes hash-based cryptography which necessitates a new signature for each transaction. The One-Time Signature (OTS) Keys must not be reused:

* **Once all OTS Key indexes are consumed, the address can no longer initiate outbound transactions.**

## Best Wallet Practices

* **Track OTS Key Usage:** Keep a record of all OTS Key indexes used in a digital spreadsheet or physical ledger.
* **Backup:** Securely backup your wallet data onto paper or other durable media.
* **Private Key Storage:** Store your private keys offline in a secure location to prevent unauthorized access.

## OTS Key Index

Creating a new wallet generates an XMSS tree filled with multiple OTS keys. Each transaction uses one OTS key index, and each key can only be used once:

* **Caution:** If you exhaust all OTS Key Indexes while funds remain in the wallet, those funds will become permanently inaccessible!

## BTQ Web Wallet Functionalities

* **New Web Wallet:** Create a new BTQ wallet using the web interface.
* **Open Web Wallet:** Access an existing BTQ wallet.
* **Send Web Wallet:** Execute transactions using the web interface.
* **Backup Web Wallet:** Securely backup your BTQ wallet.

## Checking a Wallet Balance

* With the wallet interface open, you can view your balance directly on the main screen.
* Alternatively, use the BTQ Explorer to check your balance without opening the wallet by entering your address in the search field. This will display all transactions associated with the address, along with the current balance of BTQ and any tokens.

## Finding Remaining OTS Keys

* To determine the number of remaining OTS keys, navigate to the OTS tab in the Block Explorer. Enter your address in the search bar and select the OTS tab to view which keys have been used and identify the next available key.

This comprehensive guide to using the BTQ Web Wallet ensures that users can manage their assets securely while adhering to the best practices of a quantum-resistant cryptocurrency.
