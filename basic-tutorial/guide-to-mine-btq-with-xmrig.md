---
description: >-
  This guide will walk you through the process of setting up and running XMRig
  to mine BTQ on Windows, macOS, and Ubuntu.
---

# Guide to Mine BTQ with XMRig

## **Step 1: Download and Install XMRig**

**Windows**

1. Visit the official XMRig website: [https://xmrig.com/](https://xmrig.com/).
2. Download the Windows version of XMRig.
3. Extract the downloaded file into a convenient folder.

**macOS**

1. Visit the official XMRig website: [https://xmrig.com/](https://xmrig.com/).
2. Download the macOS version of XMRig.
3. Extract the downloaded file into a convenient folder.

**Ubuntu**

1.  Open Terminal and run the following commands to update and install necessary packages:

    ```sh
    sudo apt update
    sudo apt install git build-essential cmake libuv1-dev libssl-dev libhwloc-dev
    ```
2.  Clone the XMRig repository from GitHub and build the project:

    ```sh
    git clone https://github.com/xmrig/xmrig.git
    cd xmrig
    mkdir build
    cd build
    cmake ..
    make
    ```

## **Step 2: Configure XMRig**

**Windows**

1. Open the folder where XMRig was extracted.
2. Create a new file named `start_mining.bat`.
3.  Open the file with Notepad and paste the following configuration:

    ```sh
    xmrig --donate-level 5 -o ip:port -u Address -p SiliconValleyUM --coin BTQ -a cn/1
    ```
4. Save the file and close Notepad.

**macOS and Ubuntu**

1. Open a Text Editor and create a new file named `start_mining.sh`.
2.  Paste the following configuration into the file:

    ```sh
    ./xmrig --donate-level 5 -o ip:port -u Address -p SiliconValleyUM --coin BTQ -a cn/1
    ```
3. Save the file and close the Text Editor.
4. Open Terminal and navigate to the folder containing `start_mining.sh`.
5.  Run the following command to make the script executable:

    ```sh
    chmod +x start_mining.sh
    ```



### BTQ Mining Pools

Below are the links to the Bitcoin Quantum (BTQ) mining pools:

* Silicon Valley, USA: [us.silicon-valley.pool.bitcoinq.xyz](https://us.silicon-valley.pool.bitcoinq.xyz)
* Phoenix, USA: [us.phoenix.pool.bitcoinq.xyz](https://us.phoenix.pool.bitcoinq.xyz)
* Dubai, UAE: [uae.dubai.pool.bitcoinq.xyz](https://uae.dubai.pool.bitcoinq.xyz)
* Singapore: [sg.singapore.pool.bitcoinq.xyz](https://sg.singapore.pool.bitcoinq.xyz)
* Shanghai, China: [qq.shanghai.pool.bitcoinq.xyz](https://qq.shanghai.pool.bitcoinq.xyz)
* Hong Kong: [qq.hongkong.pool.bitcoinq.xyz](https://qq.hongkong.pool.bitcoinq.xyz)
* Shanghai, China: [qq.cn-sh.pool.bitcoinq.xyz](https://qq.cn-sh.pool.bitcoinq.xyz)
* Jakarta, Indonesia: [in.jakarta.pool.bitcoinq.xyz](https://in.jakarta.pool.bitcoinq.xyz)
* Hong Kong, China: [cn.hongkong.pool.bitcoinq.xyz](https://cn.hongkong.pool.bitcoinq.xyz)

You can join any of these pools to combine computational power and share BTQ rewards efficiently.

## **Step 3: Run XMRig**

**Windows**

1. Double-click on the `start_mining.bat` file to start mining.

**macOS and Ubuntu**

1. Open Terminal.
2.  Navigate to the folder containing `start_mining.sh` using the command:

    ```sh
    cd /path/to/your/folder
    ```
3.  Run the script using the command:

    ```sh
    ./start_mining.sh
    ```

#### Parameters Explained

* `--donate-level 5`: Donation level to the developer (5%).
* `-o ip:port`: The address and port of the mining pool.
* `-u Address`: Your BTQ wallet address to receive mined coins.
* `-p SiliconValleyUM`: Worker name or pool password (depending on pool configuration).
* `--coin BTQ`: The coin you want to mine (BTQ - Bitcoin Quantum).
* `-a cn/1`: The algorithm used for mining (cn/1 - CryptoNight variant 1).

#### Notes

* Ensure you have all necessary drivers installed for your CPU/GPU.
* Check your internet connection to ensure you can connect to the mining pool.

With these steps, you are ready to start mining BTQ with XMRig on Windows, macOS, and Ubuntu. Good luck!
