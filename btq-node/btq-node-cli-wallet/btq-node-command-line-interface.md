---
description: >-
  Here's the adapted guide for interacting with the BTQ network using the
  Command Line Interface (CLI)
---

# BTQ Node Command Line Interface

## BTQ Node Command Line Interface

Interacting with the BTQ network can be done utilizing the CLI interface. This allows you to complete advanced tasks on the network. Using the CLI is straightforward, and there is a helpful `--help` section to guide you.

It is recommended that you have a local working installation of BTQ to use the CLI. Refer to the Node installation instructions to get started. Follow the guide to set up a BTQ node if you haven't already.

## **Remote Node Connection**

You can connect to a remote node that allows external connections. Use the `--host {REMOTE_IP_ADDRESS}` flag on the CLI to connect.

### **Overview**

Running commands using the BTQ node CLI requires the BTQ node software to be installed. Refer to the documentation for installation instructions and the full Node CLI documentation.

### **CLI Help**

All command line options have a help file available to assist in their usage. Simply add the `--help` option to the end of any command to see the help.

```bash
btq --help
```

### **Usage**

```bash
Usage: btq [OPTIONS] COMMAND [ARGS]...

  BTQ Command Line Interface

Options:
  -v, --verbose       verbose output whenever possible
  --host TEXT         remote host address             [127.0.0.1]
  --port_pub INTEGER  remote port number (public api) [19009]
  --wallet_dir TEXT   local wallet dir
  --json              output in json
  --version           Show the version and exit.
  --help              Show this message and exit.

Commands:
  slave_tx_generate    Generates Slave Transaction for the wallet
  state                Shows Information about a Node's State
  token_list           Fetch the list of tokens owned by an address.
  tx_inspect           Inspects a transaction blob
  tx_message           Message Transaction
  tx_multi_sig_create  Creates Multi Sig Create Transaction, that...
  tx_multi_sig_spend   Transfer coins from src to dsts
  tx_push              Sends a signed transaction blob to a node
  tx_token             Create Token Transaction, that results into...
  tx_transfer          Transfer coins from src to dsts
  tx_transfertoken     Create Transfer Token Transaction, which...
  wallet_add           Adds an address or generates a new wallet...
  wallet_decrypt
  wallet_encrypt
  wallet_gen           Generates a new wallet with one address
  wallet_ls            Lists available wallets
  wallet_recover       Recovers a wallet from a hexseed or mnemonic...
  wallet_rm            Removes an address from the wallet using the...
  wallet_secret        Provides the mnemonic/hexseed of the given...
```

**Example: `btq tx_transfer --help`**

```bash
Usage: btq tx_transfer [OPTIONS]

  Transfer coins from src to dsts

Options:
  --src TEXT               signer BTQ address
  --master TEXT            master BTQ address
  --dsts TEXT              List of destination addresses
  --amounts TEXT           List of amounts to transfer (Quanta)
  --message_data TEXT      Message (Optional)
  --fee DECIMAL            fee in Quanta
  --ots_key_index INTEGER  OTS key Index (1..XMSS num signatures)
  --help                   Show this message and exit.
```

### **Options**

These options allow advanced functionality like remote node connections.

```bash
  -v, --verbose       verbose output whenever possible
  --host TEXT         remote host address             [127.0.0.1]
  --port_pub INTEGER  remote port number (public api) [19009]
  --wallet_dir TEXT   local wallet dir
  --json              output in json
  --version           Show the version and exit.
  --help              Show this message and exit.
```

**Note:** These options must be entered directly after the `btq` command, before any sub-commands are given.

```bash
btq [OPTIONS] [COMMAND]
```

| Command Option | Comments                                                                                                                           |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `--host`       | \[default: 127.0.0.1] Host to connect to for network functions and chain data retrieval                                            |
| `--port_pub`   | \[default: 19009] Port to use to connect to node services for network functions and chain data retrieval using the node public API |
| `--wallet_dir` | Full path to the location of the `wallet.json` file to use for the function if not included in the local directory                 |
| `--json`       | Print command output as JSON data for scripting functions                                                                          |
| `--version`    | Print the version of the BTQ software and exit                                                                                     |
| `--help`       | Print the help file and exit                                                                                                       |

This guide should assist you in using the BTQ CLI for various tasks and advanced operations.
