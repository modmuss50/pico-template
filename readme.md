# Pico Template

A simple cmake template for the Raspberry Pi pico. CLion works great as an IDE.

Was made with help from the [Getting Started guide](https://datasheets.raspberrypi.org/pico/getting_started_with_pico.pdf)

# MacOS setup

```bash
brew tap ArmMbed/homebrew-formulae
brew install arm-none-eabi-gcc cmake ninja
git submodule update --init --recursive
```

# Build

```bash
mkdir build
cd build
camke -G Ninja ..
ninja
```

Copy the .uf2 onto the pico to run

# Serial console

```bash
ls /dev/tty.*
screen /dev/tty.usbmodem0000000000001
```