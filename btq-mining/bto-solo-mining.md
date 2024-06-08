---
description: Setting up solo mining for BTQ (Bitcoin Quantum)
---

# BTO Solo Mining

Setting up solo mining for BTQ (Bitcoin Quantum) involves establishing a BTQ mining node on your PC or server. This setup allows you to mine BTQ while operating a full node on the BTQ network. To start mining, you will need to enable this feature in the node's configuration file.

## Requirements

* BTQ software installed and fully synced with the network.
* A BTQ wallet address to receive mining rewards.
* Some time to complete the setup.
* Local or remote shell access (e.g., SSH).

## Preliminary Checks

Ensure you have a fully functioning BTQ node that is synced with the blockchain. If you're just starting, refer to the BTQ Node overview for setup instructions.

You can check the status of your node by entering `btq state` into the command line, which will display the Blockheight of your node and other relevant information. Make sure this matches the height shown on the BTQ explorer.

### Configuration

Navigate to the default BTQ directory and edit the configuration file located at `~/$USER/.btq/config.yml`. If it doesn’t already exist, you’ll need to create it:

```bash
nano ~/.btq/config.yml
```

Below are the default settings for mining, which are not enabled initially:

```yaml
# --------------------------------------
#    Mining Configuration
# --------------------------------------
# mining_enabled: False
# mining_address: ''
# mining_thread_count: 0  # 0 auto-detect thread count based on the number of processors
#
```

To begin mining, change the settings by removing the `#` (comment) marks, setting `mining_enabled` to `True`, entering your BTQ wallet address, and configuring the `mining_thread_count` (0 for auto-detect based on your processor count):

```yaml
# --------------------------------------
#    Mining Configuration
# --------------------------------------
mining_enabled: True
mining_address: 'YOUR_BTQ_WALLET_ADDRESS'
mining_thread_count: 0  # 0 to auto detect thread count based on CPU/GPU number of processors
#
```

### Restart BTQ Node

After configuring, restart the BTQ node to apply the new settings. You must stop the node if it's still running, to ensure it picks up the new configuration:

```bash
start_btq
```

Once your node re-syncs with the network, it will begin mining the current blocks. You will see the mined rewards in the wallet address specified in your configuration file.

You can check the status of your node anytime by running:

```bash
btq state
```

This setup will integrate your machine into the BTQ network, enabling you to contribute to network security while earning mining rewards.
