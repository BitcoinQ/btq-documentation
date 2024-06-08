---
description: BTQ Node Configuration
---

# BTQ Node Config

## BTQ Node Configuration

The BTQ node configuration allows users to customize settings via a configuration file located at `~/.btq/config.yml` in the local root BTQ directory.

**Important:** The node must be restarted to apply any modifications to the configuration if it is already running.

### **BTQ Mining Config**

Configure mining to utilize the local machine's processor.

| Directive             | Default | Description                                            |
| --------------------- | ------- | ------------------------------------------------------ |
| `mining_enabled`      | False   | Enable mining on the local node                        |
| `mining_address`      | None    | Wallet address to receive mining rewards               |
| `mining_thread_count` | 0       | Auto-detect thread count based on CPU/GPU capabilities |

**Example Mining Config:**

```yaml
##======================================
##   Mining Configuration
##======================================
mining_enabled: False
mining_address: 'Q010500f07a209bfa657e526118a9c5e40ecb5f69d3a8da991ddc1fe0269c7ec617f693f362a051'
mining_thread_count: 0
```

### **Ephemeral Config**

This function is still under development and may change in the future.

| Directive                 | Default | Description                      |
| ------------------------- | ------- | -------------------------------- |
| `accept_ephemeral`        | True    | Enable ephemeral traffic on node |
| `outgoing_message_expiry` | 90      | Message expires after 90 seconds |

**Example Ephemeral Config:**

```yaml
##======================================
##   Ephemeral Configuration
##======================================
accept_ephemeral: True
outgoing_message_expiry: 90
```

### **P2P Config**

Configure the Peer-to-Peer settings for the node.

| Directive                          | Default                             | Description                                                          |
| ---------------------------------- | ----------------------------------- | -------------------------------------------------------------------- |
| `max_redundant_connections`        | 5                                   | Max connections allowed from nodes with the same IP                  |
| `enable_peer_discovery`            | True                                | Allow discovery of new peers                                         |
| `peer_list`                        | \[IP addresses]                     | List of peers for P2P connections                                    |
| `p2p_local_port`                   | 19000                               | Locally bound port for connections                                   |
| `p2p_public_port`                  | 19000                               | Public port for forwarding connections                               |
| `p2p_q_size`                       | 10000                               | Size of the P2P queue                                                |
| `peer_rate_limit`                  | 500                                 | Max number of messages per minute per peer                           |
| `ban_minutes`                      | 20                                  | Minutes to ban offending peer IPs                                    |
| `monitor_connections_interval`     | 30                                  | Interval to monitor connections (seconds)                            |
| `max_peers_limit`                  | 100                                 | Max number of peers allowed to connect                               |
| `ntp_refresh`                      | 12                                  | Hours to refresh NTP sync                                            |
| `ntp_request_timeout`              | 10                                  | Seconds before NTP timeout                                           |
| `ntp_servers`                      | \['pool.ntp.org', 'ntp.ubuntu.com'] | NTP servers                                                          |
| `chain_state_timeout`              | 180                                 | Timeout for chain state (seconds)                                    |
| `chain_state_broadcast_period`     | 180                                 | Period for broadcasting chain state (must be less than ping timeout) |
| `transaction_pool_size`            | 25000                               | Transaction pool size                                                |
| `transaction_minimum_fee`          | 1000000000                          | Minimum transaction fee (in smallest unit)                           |
| `pending_transaction_pool_size`    | 75000                               | Size of the pending transaction pool                                 |
| `pending_transaction_pool_reserve` | 75                                  | Reserve for moving stale transactions                                |
| `stale_transaction_threshold`      | 15                                  | Blocks threshold before considering a transaction stale              |

**Example P2P Config:**

```yaml
##======================================
##   PEER Configuration
##======================================
max_redundant_connections: 5
enable_peer_discovery: True
peer_list:
 - 47.91.120.22
 - 47.242.207.111
 - 139.224.117.106
 - 8.219.202.7
p2p_local_port: 19000
p2p_public_port: 19000
p2p_q_size: 10000
peer_rate_limit: 500
ban_minutes: 20
monitor_connections_interval: 30
max_peers_limit: 100
ntp_refresh: 12
ntp_request_timeout: 10
ntp_servers:
  - 'pool.ntp.org'
  - 'ntp.ubuntu.com'
chain_state

_timeout: 180
chain_state_broadcast_period: 180
transaction_pool_size: 25000
transaction_minimum_fee: 1000000000
pending_transaction_pool_size: 75000
pending_transaction_pool_reserve: 75
stale_transaction_threshold: 15
```

### **Admin API Config**

Configure the administrative API of the BTQ node.

| Directive                      | Default     | Description                      |
| ------------------------------ | ----------- | -------------------------------- |
| `admin_api_enabled`            | False       | Enable the admin API             |
| `admin_api_host`               | "127.0.0.1" | Host for the admin API           |
| `admin_api_port`               | 19008       | Port for the admin API           |
| `admin_api_threads`            | 1           | Number of threads for admin API  |
| `admin_api_max_concurrent_rpc` | 100         | Max concurrent RPC for admin API |

**Example Admin API Config:**

```yaml
##======================================
##       ADMIN API CONFIGURATION
##======================================
admin_api_enabled: False
admin_api_host: "127.0.0.1"
admin_api_port: 19008
admin_api_threads: 1
admin_api_max_concurrent_rpc: 100
```

### **Public API Config**

Configuration settings for the public-facing API of the BTQ node.

| Directive                       | Default   | Description                       |
| ------------------------------- | --------- | --------------------------------- |
| `public_api_enabled`            | True      | Enable the public API             |
| `public_api_host`               | "0.0.0.0" | Host for the public API           |
| `public_api_port`               | 19009     | Port for the public API           |
| `public_api_threads`            | 1         | Number of threads for public API  |
| `public_api_max_concurrent_rpc` | 100       | Max concurrent RPC for public API |

**Example Public API Config:**

```yaml
##======================================
##       PUBLIC API CONFIGURATION
##======================================
public_api_enabled: True
public_api_host: "0.0.0.0"
public_api_port: 19009
public_api_threads: 1
public_api_max_concurrent_rpc: 100
```

### **Mining API Config**

Configuration settings for the mining-specific API of the BTQ node.

| Directive                       | Default     | Description                       |
| ------------------------------- | ----------- | --------------------------------- |
| `mining_api_enabled`            | False       | Enable the mining API             |
| `mining_api_host`               | "127.0.0.1" | Host for the mining API           |
| `mining_api_port`               | 19007       | Port for the mining API           |
| `mining_api_threads`            | 1           | Number of threads for mining API  |
| `mining_api_max_concurrent_rpc` | 100         | Max concurrent RPC for mining API |

**Example Mining API Config:**

```yaml
##======================================
##   Mining API Configuration
##======================================
mining_api_enabled: False
mining_api_host: "127.0.0.1"
mining_api_port: 19007
mining_api_threads: 1
mining_api_max_concurrent_rpc: 100
```

### **Debug API Config**

Configuration settings for the debug API, useful for troubleshooting and development.

| Directive                      | Default     | Description                      |
| ------------------------------ | ----------- | -------------------------------- |
| `debug_api_enabled`            | False       | Enable the debug API             |
| `debug_api_host`               | "127.0.0.1" | Host for the debug API           |
| `debug_api_port`               | 52134       | Port for the debug API           |
| `debug_api_threads`            | 1           | Number of threads for debug API  |
| `debug_api_max_concurrent_rpc` | 100         | Max concurrent RPC for debug API |

**Example Debug API Config:**

```yaml
##======================================
##        DEBUG API CONFIGURATION
##======================================
debug_api_enabled: False
debug_api_host: "127.0.0.1"
debug_api_port: 52134
debug_api_threads: 1
debug_api_max_concurrent_rpc: 100
```

### **GRPC Proxy Config**

Settings for the GRPC proxy, facilitating GRPC connections.

| Directive         | Default     | Description             |
| ----------------- | ----------- | ----------------------- |
| `grpc_proxy_host` | "127.0.0.1" | Host for the GRPC proxy |
| `grpc_proxy_port` | 18090       | Port for the GRPC proxy |

**Example GRPC Proxy Config:**

```yaml
##======================================
##       GRPC PROXY CONFIGURATION
##======================================
grpc_proxy_host: "127.0.0.1"
grpc_proxy_port: 18090
```

### **Wallet Daemon Config**

Configuration settings for the wallet daemon which handles wallet interactions via API.

| Directive            | Default           | Description                                     |
| -------------------- | ----------------- | ----------------------------------------------- |
| `public_api_server`  | "127.0.0.1:19009" | Server where the public API is available        |
| `wallet_daemon_host` | "127.0.0.1"       | Host for the wallet daemon                      |
| `wallet_daemon_port` | 18091             | Port for the wallet daemon                      |
| `number_of_slaves`   | 3                 | Number of slave processes for handling requests |

**Example Wallet Daemon Config:**

```yaml
##======================================
##      WALLET DAEMON CONFIGURATION
##======================================
public_api_server: "127.0.0.1:19009"
wallet_daemon_host: "127.0.0.1"
wallet_daemon_port: 18091
number_of_slaves: 3
```

### **Wallet API Config**

Settings for the API that allows wallet operations.

| Directive                       | Default     | Description                       |
| ------------------------------- | ----------- | --------------------------------- |
| `wallet_api_host`               | "127.0.0.1" | Host for the wallet API           |
| `wallet_api_port`               | 19010       | Port for the wallet API           |
| `wallet_api_threads`            | 1           | Number of threads for wallet API  |
| `wallet_api_max_concurrent_rpc` | 100         | Max concurrent RPC for wallet API |

**Example Wallet API Config:**

```yaml
##======================================
##        WALLET API CONFIGURATION
##======================================
wallet_api_host: "127.0.0.1"
wallet_api_port: 19010
wallet_api_threads: 1
wallet_api_max_concurrent_rpc: 100
```

