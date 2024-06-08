---
description: >-
  Explore the BTQ Wallet, your gateway to securely managing your Bitcoin Quantum
  assets.
---

# BTQ Wallet Overview

The Bitcoin Quantum Resistant Ledger (BTQ) functions similarly to other cryptocurrencies by utilizing both public and private keys that correspond to a specific address. What sets BTQ apart is its innovative approach to post-quantum security, primarily through its signature scheme.

BTQ employs the Extended Merkle Signature Scheme (XMSS), a hash-based cryptography method that has been in existence since the 1970s and was recently approved by NIST for use in cryptographic systems. XMSS is celebrated for its robust quantum-resistant properties, making it one of the most secure algorithms available today.

However, there is a notable limitation associated with hash-based cryptography: each signature key index can only be used once. This unique characteristic ensures enhanced security but requires careful management of key indices to maintain the integrity of the cryptographic system.

## BTQ Address Options

This feature in the BTQ Wallet allows users to customize the tree height, which determines the number of One-Time Signatures (OTS) available for transactions on the blockchain. By default, a tree height of 10 provides 1,024 OTS key indexes, but users have the flexibility to create wallets with either more or fewer OTS keys according to their needs.

Increasing the tree height results in a greater number of OTS Key Indexes, which enhances the security of your transactions. However, a larger tree height also means longer times for key generation. Each time the wallet is accessed, these keys need to be calculated, thus extending the time it takes to open a wallet with a higher number of addresses.

It's important to note that these parameters must be set during the creation of the wallet. The chosen height of the tree is crucial as it influences the creation of the OTS key indexes and contributes to the uniqueness of each private key. This setup is designed to optimize both security and functionality in the BTQ Wallet.

| Tree Height | Available Keys | Notes                                                       |
| :---------: | :------------: | ----------------------------------------------------------- |
|      8      |       256      | Allows 256 transactions to be **sent** from the address     |
|      10     |      1,024     | Allows 1024 transactions to be **sent** from the address    |
|      12     |      4,096     | Allows 4,096 transactions to be **sent** from the address   |
|      14     |     16,384     | Allows 16,384 transactions to be **sent** from the address  |
|      16     |     65,536     | Allows 65,536 transactions to be **sent** from the address  |
|      18     |     262,144    | Allows 262,144 transactions to be **sent** from the address |

## BTQ Hash Function

BTQ can utilize multiple hash functions, depending on the setting used during the creation of the wallet.

By default the wallet will utilize the shake128 hash function if no configuration options are given.

| Hash Function | Hash Algorithm                               | Description                                              |
| ------------- | -------------------------------------------- | -------------------------------------------------------- |
| shake128      | [SHA-3](https://en.wikipedia.org/wiki/SHA-3) | Secure Hash Algorithm 3 - Default used in the web wallet |
| sha2\_256     | [SHA-2](https://en.wikipedia.org/wiki/SHA-2) | Secure Hash Algorithm 2                                  |
| shake256      | [SHA-3](https://en.wikipedia.org/wiki/SHA-3) | Secure Hash Algorithm 3                                  |

## BTQ Wallet Security

All BTQ wallets are constructed around a cryptographic key pair, consisting of public and private keys. From these keys, a Merkle tree is generated, which is composed of One-Time Signature (OTS) key indexes. These OTS key indexes are used individually for each transaction to sign outgoing transfers. This method ensures that the root secret, or the "private" key, is never exposed during transactions. Each signature provided by an OTS key index is unique to a specific transaction, enhancing security by preventing potential reuse and exposure

{% hint style="info" %}
CAUTION:

Before interacting with the BTQ network, it is crucial for users to accurately record and securely store their private recovery keys (either mnemonic or hexphrase). After recording, verifying that these recovery keys function correctly is essential. This step is vital to ensure that your funds are not sent to an address beyond your control. Proper management and verification of your recovery keys will safeguard your assets and provide peace of mind as you engage with the BTQ network.
{% endhint %}

### Public Key

At the core of the BTQ wallet is the BTQ address. Each public key starts with a "Q" and consists of 79 hexadecimal characters. This public address serves as the account identifier and is the information you would provide to receive funds.

Public keys are safe to share with trusted parties with whom you will be transacting. You can use your public address to request funds from another user or to deposit funds into your own wallet.

**Example BTQ Public Address:**&#x20;

```
Q020500ff7195e78daa5d8b35df71372739c2080b197f1832b54710d1167be4a2587f6546f2e6f9
```

### Private Key

Private keys in the BTQ ecosystem can be represented in three forms: a hexseed, a mnemonic phrase, or a wallet.json file that contains both. Any of these forms can be used to restore a wallet, and it is crucial to follow best practices to secure these keys.

**Key Points about Private Keys:**

* **Required for Transactions:** A private key is essential for interacting with the BTQ blockchain.
* **Unique Signatures:** Private keys are used to sign transactions, ensuring that no two transactions are the same.
* **Exclusivity:** Each private key is unique; no two private keys are identical.
* **Control Over Funds:** Anyone in possession of a private key can initiate transactions on behalf of the associated address.
* **Verification:** Always ensure that any recovery keys open the expected address before using it.
* **Security:** NEVER SHARE PRIVATE WALLET KEYS. Exposure of private keys can lead to unauthorized access and potential loss of funds.

**Security Best Practices:**

* **Storage:** It is the responsibility of the user to ensure that all secret keys and encryption phrases are stored securely. Any loss of funds due to misplaced, stolen, or improperly copied keys is the sole responsibility of the owner.
* **Backup Verification:** Before depositing funds, verify that your backup method re-opens the same address as expected.
* **Irrecoverable Keys:** Private keys cannot be regenerated if lost. Without them, the funds in the address are irrecoverable. Therefore, it is vital to backup your keys and store them in secure locations.

**Typical BTQ Private Key Format:** While private keys can be stored in various formats, they are typically utilized through a wallet application to facilitate ease of use and enhance security.

**Remember:** Maintaining the confidentiality and integrity of your private keys is the most effective way to secure your assets within the BTQ network.

### **Typical BTQ Private Key Format**[**​**](https://docs.theqrl.org/use/wallet/overview#typical-qrl-private-key-format)

Public and private keys can be stored in a multitude of ways and are typically utilized through a wallet application.

| Private Key Medium | Information                                                                                                                                                                                                                                                                                                          |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `wallet.json` file | <ul><li>Contains both Hexphrase and Mnemonic as well as the Public Key</li><li>May be encrypted <em>(recommended)</em> and passphrase will be required to open</li><li>Generated from the Desktop, Web and CLI wallet applications</li></ul>                                                                         |
| Mnemonic Phrase    | <ul><li>Wordlist consisting of 34 selected words from the master BTQ wordlist</li><li>Available using backup functions of the wallet applications</li><li>Provided during most address generation steps</li></ul>                                                                                                    |
| Hexphrase          | <ul><li>Available using backup functions of the wallet applications</li><li>Hexstring consisting of 102 mixed alpha numeric characters</li><li>Provided during most address generation processes, or found in a "Backup Wallet" function</li></ul>                                                                   |
| Ledger Hardware    | <ul><li>Ledger manages BTQ private keys on device, never exposing them to the end user</li><li>Master Ledger Recovery Seed is required to recover a BTQ address stored on a Ledger device</li></ul>                                                                                                                  |
| Slave Keys         | <ul><li>Advanced address functionality. CLI tools are required to generate slave Keys</li><li>Generated slaves files are typically named <code>slaves.json</code> or <code>payment_slaves.json</code></li><li>Slave keys are additional secret key(s) that are allowed to spend for a given master address</li></ul> |



{% hint style="info" %}
**NEVER SHARE PRIVATE WALLET KEYS**

These keys should never be shared! Anyone can transfer funds using a secret key.
{% endhint %}

**Example BTQ Mnemonic**[**​**](https://docs.theqrl.org/use/wallet/overview#example-qrl-mnemonic)

This list of 34 works represents the same key as the hexseed, with each word corresponding to an index location in the BTQ wordlist. This list is converted into binary/hexadecimal representation of the private keys.

```
action filled polish crunch luther sermon heap afraid stifle palm oyster fruity joyous loose sweat plane mud alley gravel rest tank mortar sham rear clown intend clue pelvis wrap moat piggy feeble toward solar
```

**Example BTQ Hexseed**[**​**](https://docs.theqrl.org/use/wallet/overview#example-qrl-hexseed)

```
020500a7b344845c3a67003cd699e59d558975081edc3a56916063607b5edec8fdc4db222ca7152cca14fd48dda394e0e81cec
```
