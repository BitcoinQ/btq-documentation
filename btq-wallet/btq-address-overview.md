---
description: The BTQ (Bitcoin Quantum) address
---

# BTQ Address Overview

The BTQ (Bitcoin Quantum) address serves as a key element in the blockchain ecosystem, representing a user's wallet as a publicly shareable identity that safely holds funds.

## Public Address

The BTQ public address acts as a visible identifier that allows others to send funds to the wallet. It is cryptographically paired with a private key.

**Typical BTQ Public Address Format:** A BTQ public address, usually starting with the letter "Q," looks like this: Q000400202ea4dc2b83ded8cfcd4fc8c0447ca3391582430cec6b093291ab9773173af1bb5ed7e8. This 79-character hexadecimal string is unique to its corresponding private key.

Sharing the public key is generally safe as the funds are not accessible with the public address alone. However, because the balance is visible on the blockchain explorer, sharing it can pose a personal security risk, akin to disclosing your bank account balance. Caution is advised when sharing this information.

## Private Keys

The private key associated with a BTQ public address is crucial for on-chain interactions and accessing funds.

### **Key Points About Private Keys:**

* **Generation:** Private keys are generated using BTQ wallets. Once generated, the key pair cannot be changed.
* **Security:** The private key should never be shared. It provides full access to the wallet's funds and is considered highly sensitive.

## Mnemonic Phrase

A mnemonic phrase is a user-friendly series of words that represent the wallet's seed. It's less prone to errors than other seed forms and provides an accessible way to restore or transfer wallet information.

**Example Mnemonic Phrase:** aback drank swap fence strait donor script form imply eerie invade brave fan legend tape evil higher ride mortar tricky expect gentry scare retire remark gritty wolves repeal weary gray peak blew tsar pipe

## Hexseed

The hexseed is another representation of the wallet's seed, presented in a hexadecimal format. Like the mnemonic phrase, it can regenerate the full Merkle tree when entered into the wallet software.

**Example Hexseed:** 000400dbf4ead7e3eec1155b6ea44b7181c94cb7cadee49969eb798fdea34ad5c3c01b64b4661dfbeb51f76609a0c182eb7a47

## Wallet.Json File

The wallet.json file is a comprehensive digital wallet file that contains all essential wallet information, including the public address, private key (seed), hexseed, mnemonic phrase, and more.

**Important:**

* **Security:** This file should always be encrypted and never shared publicly, as it grants complete access to the wallet.
* **Storage:** Careful consideration should be given to how and where this file is stored to prevent unauthorized access.

Here's an example structure of what a wallet.json file might contain, showing the unencrypted format for clarity:

```json
[
  {
    "address":"Q0105002c84abbc4e364a0b9b98d748e06d11b1916fda745f7370c024ec015633608db39e21c4d6",
    "addressB32":"q1qyzsqtyy4w7yudj2pwde346gupk3rvv3dld8ghmnwrqzfmqp2cekprdn2kstr0",
    "pk":"010500aeaa4afa476b57235a0bb0204d4a689c997e7ef625d771545186ca2f162f41ecf6f9a3b285631b123f5a452dfcaeb12473171e01e0d1e52c6b36ba8948055028",
    "hexseed":"01050056f9aa2189bca075d93043e958d0c5434f34149b4bb8d44e243a8a4119f9427d02a65fcef820f504f7831eae906ba67d",
    "mnemonic":"absorb filled frank opaque byte ornate pause gleam corps dome full assert ear vigil behind remove rival effort card pore drool pass dusk sorrow plight worse wet axes air knock bubble trance horrid hedge",
    "height":8,
    "hashFunction":{},
    "signatureType":{},
    "index":0,
    "walletType":"seed",
    "encrypted":false
  }
]
```

This file can be uploaded to the wallet software encrypted or unsecured, and will allow the wallet software to regenerate the full Merkle tree for the given address, facilitating full interaction with the blockchain and access to all funds.
