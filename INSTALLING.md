# Toolchain
This guide is written for 64-bit Ubuntu, and alike. It also works with WSL (Windows Subsystem for Linux).

## Apt packages
Install required packages needed for building some tools: `sudo apt install build-essential texinfo`

Installation path /opt is assumed for all toolchain components. However, this is not restricted and your installation location may vary.

## Compiler
Small Device C Compiler (SDCC) version 4.0.0 was used in this project.
* Download SDCC from https://sourceforge.net/projects/sdcc/files/sdcc-linux-amd64/4.0.0/
* Unzip to /opt: `sudo cd /opt && sudo tar xf sdcc-4.0.0-amd64-unknown-linux2.5.tar.bz2`
* Verify architecture compatibility: `/opt/sdcc-4.0.0/bin/sdcc -v`

## Binutils (optional)
Binutils can be used to inspect the compiled binary and debug the MCU. Installing these tools is optional.
* Download stm8 binutils-gdb from https://sourceforge.net/projects/stm8-binutils-gdb/files/, version 2020-03-22 was used, but any newer should work as well.
* Unzip to temporary location: `tar xf stm8-binutils-gdb-sources-2020-03-22.tar.gz`
* Download binutils packages: `cd stm8-binutils-gdb-sources && ./patch_binutils.sh`
* Configure: `./configure_binutils.sh`
* Build: `cd binutils-2.30 && make`
* Install: `PREFIX=/opt/stm8-binutils sudo make install`

# Target support files

The listed packages are already downloaded and stored in the repo, but this guide is left for reference.

## STM8 Standard Peripherals Library (SPL) for SDCC

See [this wonderful project](https://github.com/gicking/STM8-SPL_SDCC_patch) for how to get community-wrangled SPL environment, ready for SDCC.
STM8L10x is supported by this repo, but STM8L15x, STM8S and STM8L5 support could be added.
