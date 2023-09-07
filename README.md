![image](https://raw.githubusercontent.com/Lumanex-Project/Lumanex/main/src/config/logo-small.png)

```
LICENSES:

// Copyright (c) 2012-2017, The CryptoNote developers, The Bytecoin developers 
// Copyright (c) 2014-2018, The Monero Project 
// Copyright (c) 2018-2019, The TurtleCoin Developers
// Copyright (c) 2023, The Lumanex Team
```

[Website](https://lumanex.org) | [Official Pool](https://pool.lumanex.org/) | [Official Block Explorer](https://explorer.lumanex.org/) | [Discord](https://discord.gg/v6ky9QPPkW) | [Twitter](https://twitter.com/LumanexProject)

![Download Count](https://img.shields.io/github/downloads/Lumanex-Project/Lumanex/total.svg)
![Open Issue Count](https://img.shields.io/github/issues/Lumanex-Project/Lumanex)
![Version](https://img.shields.io/github/v/release/Lumanex-Project/Lumanex)

**** 

### Coin specifications:

|Ticker|Decimals|Supply|Block Reward|Block Time|P2P Port|RPC Port|Service Port|Algo
|--|--|--|--|--|--|--|--|--|
|LNX|8|75,000,000 LNX|1 LNX|10 Seconds|45000|45001|45002|Chukwa Argon2id|

****

### Installing

You can download the latest binary images from here: https://github.com/Lumanex-Project/Lumanex/releases
To compile the binaries yourself, scroll down to the next section.

****

### Ubuntu 64 bit Compiling

##### Prerequisites

You will need the following packages: boost, cmake (3.8 or higher), make, git and GCC/G++ (GCC-7.0 or higher).

##### Commands

- `sudo apt-get install software-properties-common`
- `sudo add-apt-repository ppa:ubuntu-toolchain-r/test -y`
- `sudo apt-get update`
- `sudo apt-get install aptitude -y`
- `sudo aptitude install -y build-essential g++-8 gcc-8 git libboost-all-dev python3-pip`
- `sudo pip install cmake`
- `export CC=gcc`
- `export CXX=g++`
- `git clone -b master --single-branch https://github.com/Lumanex-Project/Lumanex`
- `cd Lumanex`
- `mkdir build`
- `cd build`
- `cmake ..`
- `make` *(To compile with a different amount of threads, use `make -j4` and replace the 4 with the your desired thread amount.)*

When the build process is complete. You can find the binary in `Lumanex/build/src`.

- `cd src`
- `./Lumanexd --version`

****
### Windows 64 bit Compiling

##### Prerequisites
- Install  [Visual Studio 2017 Community Edition](https://github.com/Lumanex-Project/Lumanex/raw/main/downloads/vs_community.exe)
- When installing Visual Studio, it is  **required**  that you install  **Desktop development with C++**
- Install [Boost 1.68](https://sourceforge.net/projects/boost/files/boost-binaries/1.68.0/boost_1_68_0-msvc-14.1-64.exe/download)

##### Commands
- [Download](https://github.com/Lumanex-Project/Lumanex/archive/master.zip) the GitHub repository and extract it somewhere.
- From the start menu, open 'Developer Command Prompt for VS 2017'.
- `cd <your_lumanex_location>`
- `mkdir build`
- `cd build`
- `set PATH="C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\CommonExtensions\Microsoft\CMake\CMake\bin";%PATH%`
- `cmake -G "Visual Studio 15 2017 Win64" .. -DBOOST_ROOT=C:/local/boost_1_68_0`

When it's done creating the cmake files you go ahead and open the `Lumanex/build/Lumanex.sln` file.
On the top right corner you see `Debug` and `x64` next to the `green play button`. Change `Debug` to `Releases`.  Then click on `Build` on the top menu and hit `Build Solution`. When the build process is complete. You can find the binary in `Lumanex/build/src/Releases`.

****

### OSX/Apple 64 bit Compiling

##### Prerequisites

-   Install XCode and Developer Tools.

##### Commands

-   `which brew || /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
-   `brew install --force cmake boost llvm gcc@8`
-   `export CC=gcc-8`
-   `export CXX=g++-8`
-   `git clone -b master --single-branch https://github.com/Lumanex-Project/Lumanex`
-   `cd Lumanex`
-   `mkdir build`
-   `cd build`
-   `cmake ..`
- `make` *(To compile with a different amount of threads, use `make -j4` and replace the 4 with the your desired thread amount.)*

When the build process is complete. You can find the binary in `Lumanex/build/src`.

- `cd src`
- `./Lumanexd --version`

****
### Raspberry Pi 3 B+ (AARCH64/ARM64) Compiling
The following images are known to work. Your operation system image  **MUST**  be 64 bit.

##### Known working images

-   [https://github.com/Crazyhead90/pi64/releases](https://github.com/Crazyhead90/pi64/releases)
-   [https://fedoraproject.org/wiki/Architectures/ARM/Raspberry_Pi#aarch64_supported_images_for_Raspberry_Pi_3](https://fedoraproject.org/wiki/Architectures/ARM/Raspberry_Pi#aarch64_supported_images_for_Raspberry_Pi_3)
-   [https://archlinuxarm.org/platforms/armv8/broadcom/raspberry-pi-3](https://archlinuxarm.org/platforms/armv8/broadcom/raspberry-pi-3)

Once you have a 64 bit image installed, setup proceeds the same as any Linux distribution. Ensure you have at least 2GB of ram, or the build is likely to fail. You may need to setup swap space.

##### Commands

-   `git clone -b master --single-branch https://github.com/Lumanex-Project/Lumanex`
-   `cd Lumanex`
-   `mkdir build`
-   `cd build`
-   `cmake ..`
-   `make`

When the build process is complete. You can find the binary in `Lumanex/build/src`.

- `cd src`
- `./Lumanexd --version`

****

### Thanks to these people to make Lumanex happen
Cryptonote Developers, Bytecoin Developers, Monero Developers, Forknote Project, TurtleCoin Community, Lumanex Team.

****
