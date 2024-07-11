---
description: Installing a BTQ node
---

# BTQ Node Installation

## BTQ Node Installation

Installing a BTQ node is straightforward and can be done on most modern operating systems. The installation depends on Python 3.6 or newer and the `pip3` Python package manager.

### **Minimum Node Hardware Requirements**

Basic requirements must be met to run a BTQ node efficiently. For detailed requirements, refer to the BTQ Node Requirements documentation.

## **Node Installation Instructions**

### **For Ubuntu and RedHat**

#### **BTQ RedHat Installation**

Follow these instructions to install a BTQ Node on a RedHat-based system:

1.  **Update packages**

    ```bash
    sudo dnf update
    ```
2.  **Enable Codeready Linux Builder repo for developer tools**

    ```bash
    subscription-manager repos --enable codeready-builder-for-rhel-8-x86_64-rpms
    ```
3.  **Install requirements**

    ```bash
    sudo dnf install swig make gcc gcc-c++ redhat-rpm-config python36-devel python2-devel dnf-plugins-core boost-devel openssl-devel hwloc-devel
    ```
4. **Install latest CMAKE-3.21 from sources**
   *   Remove old cmake if exists:

       ```bash
       sudo dnf remove cmake
       ```
   *   Get and install the latest cmake:

       ```bash
       wget https://github.com/Kitware/CMake/releases/download/v3.21.3/cmake-3.21.3.tar.gz
       tar -xvf cmake-3.21.3.tar.gz
       cd cmake-3.21.3 && ./bootstrap && make && sudo make install
       ```
5.  **Upgrade pip to latest version**

    ```bash
    pip3 install --user --upgrade pip
    ```
6.  **Install latest Python packages**

    ```bash
    pip3 install --user service-identity==21.1.0 wheel -U setuptools
    ```
7.  **Install BTQ**

    ```bash
    pip3 install --user -U bitcoinq
    ```

Here's the adapted installation guide for the BTQ node on Ubuntu:

#### BTQ Ubuntu Installation

Installation instructions for the BTQ Node on Ubuntu.

Tested on the latest LTS version, Ubuntu 20.04.

1.  **Update and Upgrade Software Packages**

    ```bash
    sudo apt update && sudo apt upgrade -y
    ```
2.  **Install the required packages for BTQ**

    ```bash
    sudo apt-get -y install swig3.0 python3-dev python3-pip build-essential pkg-config libssl-dev libffi-dev libhwloc-dev libboost-dev cmake libleveldb-dev
    ```
3.  **Install the latest setuptools**

    ```bash
    pip3 install -U setuptools
    ```
4.  **Install the latest service identity package**

    ```bash
    pip3 install service-identity==21.1.0
    ```
5.  **Install BTQ**

    ```bash
    pip3 install -U bitcoinq
    ```

This guide should help you set up a BTQ node on Ubuntu efficiently.

### **Running BTQ**

After successful installation, BTQ command line tools are available for interaction with the node.

*   **Start BTQ** To begin the syncing process, run:

    ```bash
    start_btq
    ```

    Expected output:

    ```
    2021-09-25 18:22:28,045|2.1.2 python|unsynced|MainThread | INFO : grpc public service - started !
    2021-09-25 18:22:29,049|2.1.2 python|synced  |MainThread | INFO : Status changed to ESyncState.synced
    ```
*   **Help for `start_btq` command**

    ```bash
    start_btq -h
    ```

    This will display all available command options for running the BTQ node, similar to the `start_btq` command, adapted for BTQ specifics.

### **Systemd Service for BTQ Node**

Set up BTQ node to start at boot and restart automatically using systemd:

1.  **Create systemd service file**

    ```bash
    sudo touch /etc/systemd/system/btq.service
    ```
2. **Edit the `btq.service` file** Use your preferred editor to add configurations that match your setup.
3.  **Enable and start the service**

    ```bash
    sudo systemctl enable btq.service
    sudo systemctl start btq.service
    ```
4.  **Check service status**

    ```bash
    sudo systemctl status btq.service
    ```

### **Crontab Script**

To ensure the BTQ node starts upon reboot, use a crontab entry:

1.  **Create and edit start-node script**

    ```bash
    nano ~/start-node.sh
    ```

    Add the following:

    ```bash
    #!/bin/bash
    screen -dmS BTQ /home/user/.local/bin/start_btq
    ```
2.  **Make the script executable**

    ```bash
    chmod +x ~/start-node.sh
    ```
3.  **Edit crontab to run the script at reboot**

    ```bash
    crontab -e
    @reboot /home/$USER/start-node.sh
    ```
