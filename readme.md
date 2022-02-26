# Pico Template

A simple C/C++ template for the Raspberry Pi pico using cmake.

[CLion](https://www.jetbrains.com/clion/) works great as an IDE.

Was made with help from the [Getting Started guide](https://datasheets.raspberrypi.org/pico/getting_started_with_pico.pdf)

# Requirements
### MacOS

```bash
brew tap ArmMbed/homebrew-formulae
brew install arm-none-eabi-gcc cmake ninja
```

### Debian/Ubuntu

```bash
sudo apt update
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi build-essential ninja-build
```

### Windows

[Windows Subsystem for Linux (WSL)](https://docs.microsoft.com/en-us/windows/wsl/install) can be used to run Ubuntu.

# Setup

Updates the [pico-sdk](https://github.com/raspberrypi/pico-sdk) sub-module, this may take a few minutes as its quite large.

```bash
git submodule update --init --recursive
```

# Build

Creates a new `build` directory and uses [ninja](https://ninja-build.org/) to build the .uf2 file.

```bash
mkdir build
cd build
cmake -G Ninja ..
ninja
```

Copy the .uf2 file from the `build` directory onto the pico to run

# Serial console (MacOS)

```bash
ls /dev/tty.*
screen /dev/tty.usbmodem0000000000001
```
