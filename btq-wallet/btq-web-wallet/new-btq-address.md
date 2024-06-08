---
description: Creating a new BTQ (Bitcoin Quantum) address
---

# New BTQ Address

Creating a new BTQ (Bitcoin Quantum) address is both simple and secure. Start by visiting the BTQ web wallet at [https://wallet.bitcoinq.xyz](https://wallet.bitcoinq.xyz).

## Backup and Verify the Address Recovery Media

Before transferring any funds to your new address, ensure that you can access the address using your backup media!

From the main menu of the BTQ web wallet, select the "New Wallet" tab to begin.

## Set a Strong Password

Enter a strong password in the provided field. The password should be at least 8 characters long and include at least one number and one letter.

## Optional Wallet Configuration

While the default settings are suitable for most users, you have options to customize your wallet further:

### **Tree Height**

This setting determines the size of the XMSS tree, which controls the number of One-Time Signatures (OTS) your wallet can use safely on the blockchain.

* **Tree Height 8:** Provides 256 OTS keys.
* **Tree Height 10:** Provides 1,024 OTS keys.
* **Tree Height 12:** Provides 4,096 OTS keys.
* **Tree Height 14:** Provides 16,384 OTS keys.
* **Tree Height 16:** Provides 65,536 OTS keys.
* **Tree Height 18:** Provides 262,144 OTS keys.

A higher tree height means more time required to generate the keys but allows more transactions before needing a new address.

### Hash Functions

You can choose from multiple secure hash functions for your wallet. By default, BTQ wallets use the SHA-3 based shake128 hash function, but other options are available:

* **shake128 (SHA-3):** Default hash function used in the web wallet.
* **sha2\_256 (SHA-2):** An alternative option.
* **shake256 (SHA-3):** Another SHA-3 variant.

All selected hash functions are secure, and the default is typically sufficient for most users.

## Create Wallet

After setting your password and adjusting the configuration settings, click the "Create Wallet" button. A new wallet will be generated, and a sensitive screen will display your:

* **Public BTQ Address:** Your wallet's public identifier.
* **Mnemonic Phrase:** A list of words that store all the information needed to recover your wallet.
* **Hexseed:** A hexadecimal string that also can recover your wallet.

## Important: Record Your Private Keys!

It is crucial to securely record your private keys. Consider saving a secure, encrypted wallet.json file, which will require your password to access. Do not forget this password!

Welcome to the realm of Quantum Resistance with BTQ!
