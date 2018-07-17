# XMRig Guide for DERO

XMRig uses separate miners for CPU and GPU, you need to download a CPU and GPU miner separately and run two separate instances on your computer.

## Downloading and Installing for Windows

XMRig has separate miners for CPU and GPU. You can download them from here:

* [XMRig CPU Miner](https://github.com/xmrig/xmrig/releases) (Use the one with `gcc` in its name)
* [XMRig GPU Nvidia Miner](https://github.com/xmrig/xmrig-nvidia/releases) (If you a 750 Ti or older, use the `cuda8` version. If you have a newer GPU, use the `cuda9` version)
* [XMRig GPU AMD Miner](https://github.com/xmrig/xmrig-amd/releases)

**Note:** You will need to download and run two separate instances if you want to mine with your GPU and CPU at the same time.

## Downloading and Installing for Mac

Needs to be compiled. Instructions [here](https://github.com/xmrig/xmrig/wiki/OS-X-Build).

## XMRig Setup and Configuration

### XMRig Configuration

1.  Unzip the file and extract the files into a new folder (Make sure your anti-virus doesn't delete the files)
2.  Open the `config.json` file with Notepad
3.  Find and change the following lines:

    * `"url: "failover.xmrig.com:443",`

    * `"user: "YOUR_WALLET",``

    - In place of `failover.xmrig.com:443`, you'll need to choose a pool to mine towards. You can check the full list [here](Pools). Make sure to keep the `"`!  Example-

    ```
    "url: "pool.dero.live:5555",
    ```

    - Instead of `YOUR_WALLET`, simply paste your public DERO address. Make sure to keep the `"`! Example-

    ```
    "user: "dERoSwiT77kefenBf5xuRY6YxX7c8f5VJWbYjXgHmXhGYWMiWVNqBM43d2E8PNE1fo9rj2VDsL7m3BntKBPKdzai5ZmqmSoMVX",
    ```

    - If you don't have one yet, you can view a [guide](../wallets/Using-the-CLI-Wallet.md#creating-a-wallet) on how to make one!


4.  Save the file and:
    * start `xmrig.exe` if you're mining with your CPU,
    * `xmrig-amd.exe`. if you're mining with an AMD GPU,
    * or `xmrig-nvidia.exe` if you're mining with a nVidia GPU.



**Remember:** if you want to mine with both your CPU and your GPU you must have both programs open at the same time!



That's it! You should be mining away now! :)
