# Edge Impulse firmware for ST Nucleo board STM32F413ZH with X-Nucleo-IKS01A3 and ESP8266 module

[Edge Impulse](https://www.edgeimpulse.com) enables developers to create the next generation of intelligent device solutions with embedded Machine Learning. This repository contains the Edge Impulse firmware for the ST B-L475E-IOT01A development board. This device supports all Edge Impulse device features, including ingestion, remote management and inferencing.

> **Note:** Do you just want to use this development board with Edge Impulse? No need to build this firmware. See the instructions [here](https://docs.edgeimpulse.com/docs/unboxing-the-st-b-l475e-iot01a) for a prebuilt image and instructions. Or, you can use the [data forwarder](https://docs.edgeimpulse.com/docs/cli-data-forwarder) to capture data from any sensor.

## Requirements

**Hardware**

* ST Nucleo board STM32F413ZH development board.

**Software**

* [Node.js 10.16](https://nodejs.org/en/download/) or higher.
* [Git](https://git-scm.com/downloads) - make sure `git` is in your PATH.
* [Mercurial](https://www.mercurial-scm.org) - make sure `hg` is in your PATH.
* [GNU ARM Embedded Toolchain 9-2019-q4-major](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads).
* STLink tools.

    Installation via Homebrew is the easiest:

    ```
    $ brew install stlink
    ```

* [Mbed CLI](https://github.com/ARMmbed/mbed-cli).

    Installation via pip is the easiest:

    ```
    $ pip install mbed-cli
    ```

Unpack the GNU ARM Embedded Toolchain, and configure Mbed CLI to use it via:

```
$ mbed config -G GCC_ARM_PATH ~/toolchains/gcc-arm-none-eabi-9-2019-q4-major/bin/
$ mbed config -G TOOLCHAIN GCC_ARM
$ mbed config -G PROTOCOL SSH
```

## Building the device firmware

