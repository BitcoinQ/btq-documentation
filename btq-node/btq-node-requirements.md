---
description: >-
  To operate a BTQ (Bitcoin Quantum) node, your system must meet specific
  requirements.
---

# BTQ Node Requirements

To operate a BTQ (Bitcoin Quantum) node, your system must meet specific requirements. This guide provides the minimum hardware and software requirements necessary to run a BTQ node effectively.

## Hardware Requirements

### **AES-NI and AVX2**

A processor with AES-NI support is crucial for the cryptographic functions of BTQ. AES enhances security, while AVX2, utilized by the Keccak hashing library, boosts hashing performance.

### **Compatibility Check**

To verify if your processor supports AES-NI and AVX2, use the following commands in a UNIX shell:

```bash
grep -m1 -o -E 'avx|aes' /proc/cpuinfo
```

Alternatively, you can use `lscpu`:

```bash
lscpu | grep -E 'aes|avx'
```

These commands will indicate if your system is compatible by showing supported features.

## **HDD Storage**

Sufficient storage is necessary to accommodate the blockchain's current and future growth. The BTQ node software syncs every block from its genesis, ensuring your node remains aligned with the network consensus.

## **Reliable Network Connection**

An uninterrupted network connection is essential as the node frequently exchanges data with others in the network, maintaining synchronization with the blockchain's current state.

## **Externally Reachable Node**

For a node to validate and relay blocks effectively, it must be externally accessible. This typically requires advanced configuration, including opening specific ports and ideally using a static IP address.

### **Modern 64-bit Processor**

A modern processor is recommended to support AES-NI and to ensure efficient node operations.

### Software Requirements

* **Python 3.6 or later**: The node software for BTQ is developed using Python, emphasizing the need for a recent version to support all functionalities.

These guidelines will help you set up and run a BTQ node, contributing to the network while ensuring robust performance and security.
