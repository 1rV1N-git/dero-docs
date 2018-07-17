# How to Mine DERO with an SBC

This guide will get you started mining DERO on a Raspberry Pi or similar SBC(single-board computer)

## Setup

Make sure you've already created a wallet on your PC. You'll need the wallet address to store any coins you mine. Follow the guide [here](../wallets/Using-the-CLI-Wallet) to get started(follow the guide for Linux).

For the SBC, download the latest non-desktop version of [Raspbian](https://www.raspberrypi.org/downloads). Follow their installation guide on how to write the OS image onto the MicroSD card. Once you've plugged in the SD Card, booted the Raspberry Pi, and connected it to the internet, run the following commands:

```
sudo apt-get update && sudo apt-get upgrade
```

This may take a few minutes. Next, we'll have to install some required tools to compile and run the miner. Enter this command:

```
sudo apt-get install git automake autoconf pkg-config libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev make g++
```

## Install the Miner

Next, we need to obtain a CPU miner. We'll use `rPi-xmrig-gcc7.3.0`

1. Download the `.zip` source code from the [Releases page](https://github.com/auto-joe/rPi-xmrig-gcc7.3.0/releases/latest)

```
wget https://github.com/auto-joe/rPi-xmrig-gcc7.3.0/archive/2.6.0-beta1.zip
```

2. Download it to a directory of your choice and extract it to a folder called `rPi-xmrig`, or anything of your choice.

```
unzip 2.6.0-beta1.zip -d / rPi-xmrig
```

## Configure and Run the Miner

Open the file `start.sh` with a text editor and replace the existing parameters with these-

```shell
./xmrig -a cryptonight -u dERo... -p x -o [pool address]
```

* Instead of `dERo...`, simply paste your DERO wallet address.

  If you don't have one yet, you can view a [guide](../wallets/Using-the-CLI-Wallet.md#creating-a-wallet) on how to make one!

* In place of `[pool address]`, you'll need to choose a pool to mine towards. You can check the full list [here](Pools).

Then start the miner-

```shell
./start.sh
```

After entering this command, the miner will start scanning your hardware and begin to mine.

Happy mining! :)
