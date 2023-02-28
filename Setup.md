## How to set up Developpement on the GPS Card:

\- **1. Kicad Setup:**

- Clone [Framework's Expansion Card Repo](https://github.com/FrameworkComputer/ExpansionCards) and follow the instruction to add it to the Template Folder.

- Edit the board in KiCad.
- Do ????? modifications to fix _"insert issue name here"_
- Profit

\- **2. RP2040/Pico SDK Setup (taken from the [_Getting started with Raspberry Pi Pico guide_](https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf) ):**

- **Create directory to house the Pico SDK:**

         cd ~/

         mkdir pico

         cd pico

- **Clone _pico-sdk_ and _pico-examples_ Git repositories :**

        git clone https://github.com/raspberrypi/pico-sdk.git --branch master

        cd pico-sdk

        git submodule update --init

        cd ..

        git clone https://github.com/raspberrypi/pico-examples.git --branch master

- **Get the LoRa Stack:**

        git clone --recurse-submodules https://github.com/sandeepmistry/pico-lorawan.git

        cd pico_lorawan

- **Install the toolchain :**

        sudo apt update

        sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi build-essential libstdc++-arm-none-eabi-newlib
