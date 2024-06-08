---
description: Backing up your BTQ (Bitcoin Quantum) Web Wallet
---

# Backup

Backing up your BTQ (Bitcoin Quantum) Web Wallet is an essential step to ensure the security of your digital assets. Here’s how you can securely back up your wallet address using the BTQ Web Wallet.

## General Information

The BTQ Web Wallet provides several methods for backing up your wallet during and after the address creation process. These methods will allow you to recover your wallet in the future.

## **Recovery Key Mediums**

* **Mnemonic Phrase:** A wordlist of 34 selected words from the master BTQ wordlist. Typically provided during the wallet creation process and available through the backup functions of the wallet applications.
* **Hexphrase:** A hexstring consisting of 102 mixed alphanumeric characters, also provided during most address generation processes or found in the "Backup Wallet" function.
* **wallet.json file:** Contains both Hexseed and Mnemonic as well as the Public Key. This file may be encrypted (recommended) and will require a passphrase to open. It is generated from the desktop, web, and CLI wallet applications.

### Strong, Long-lasting Backup Methods

It is crucial to store your backup data securely. Strong, durable methods like physical media or encrypted digital files are recommended for successful long-term backup.

### Test Your Backups!

It is vital to test your backups immediately after creation by trying to open the wallet using the backed-up data. This ensures the backup is correct and will function when needed.

## Backup Process

### **During Address Creation**

When you create a new address, the web wallet will prompt you to save the private details of your new address. You can choose to:

* Write down the mnemonic phrase or hexseed on paper and store it in a secure location.
* Save a copy of the wallet.json file in multiple locations. If encrypted, the file uses AES encryption with a passphrase you set during address creation.

### **Backup an Existing Wallet**

After creating an address, you can access the recovery seed at any time:

* In the BTQ Web Wallet, go to the "Receive" tab and select "View Recovery Seed."
* This will display the hexseed, mnemonic phrase, and a QR code containing this information.
* Securely copy this information onto another medium, such as a flash drive or external hard drive, and store it in a safe place.

### Recovering a Backup

To recover a BTQ wallet, you will need access to the secret keys associated with the address:

1. Open the web wallet software and choose to open an address.
2. Select the backup format (mnemonic phrase, hexseed, or wallet.json file) from the dropdown.
3. Enter the relevant data in the field and select "Unlock Wallet."
4. If using an encrypted wallet file, also enter the encryption passphrase.

The wallet will then load, showing all transactions related to this address.

## Troubleshooting Backup Wallets

If issues arise when opening the wallet:

* Verify the wallet.json file in a text editor to ensure it's in JSON format and check if the correct encryption passphrase is being used.
* Remember, without the correct encryption passphrase, the encrypted wallet file cannot be accessed.

By following these steps, you can effectively back up and secure your BTQ wallet, safeguarding your digital assets against potential threats or losses.
