---
title: "NVIDIA Jetson TX1"
excerpt: "The Jetson TX1 is a new board in NVIDIA embedded board family. This new board has new performance oriented for robotics application, drones, and other. In fact, this board has a compact form factor in only 50mm x 90mm."
header:
  teaser: /assets/review/NVIDIA-jetson-tx1/jetsonTX1.jpg
categories:
  - Review
tags:
  - NVIDIA
  - Jetson
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
gallery:
  - url: /assets/review/NVIDIA-jetson-tx1/core_and_carrier_tx1.jpg
    image_path: /assets/review/NVIDIA-jetson-tx1/core_and_carrier_tx1.jpg
    alt: "Jetson TX1 development board"
    title: "Jetson TX1 development board"
  - url: /assets/review/NVIDIA-jetson-tx1/TX1_core_front.jpg
    image_path: /assets/review/NVIDIA-jetson-tx1/TX1_core_front.jpg
    alt: "Jetson TX1 core – front"
    title: "Jetson TX1 core – front"
  - url: /assets/review/NVIDIA-jetson-tx1/TX1_core_back.jpg
    image_path: /assets/review/NVIDIA-jetson-tx1/TX1_core_back.jpg
    alt: "Jetson TX1 core – back"
    title: "Jetson TX1 core – back"
---

The Jetson TX1 is a new board in NVIDIA embedded board family. This new board has new performance oriented for robotics application, drones, and other. In fact, this board has a compact form factor in only **50mm x 90mm**. Jetson TX1 has:

* [NVIDIA Tegra X1 core](http://www.nvidia.com/object/tegra-x1-processor.html)
* Onboard WiFi and bluetooth
* Impressive dissipator with fan
* Industrial connector

An NVIDIA Tegra X1 core is based from [Maxwell™](https://developer.nvidia.com/maxwell-compute-architecture) architecture and has 256 GPU core and 8 ARM CPU 64-bit. This chip is build in 20 nm SOC. It is designed for low power consumption, this is really important for drones application, when the energy saving is the first issue to solve.

| | Tegra X1 |
|-|----------|
| GPU | **NVIDIA Maxwell 256-core GPU**<br/>DX-12, OpenGL 4.5, NVIDIA CUDA®, OpenGL ES 3.1, and AEP |
| CPU | **8 CPU-core, 64-bit ARM® CPU**<br/>4x A57 2MB L2; 4x A53 512KB L2 |
| POWER | **20 nm SOC – TSMC**<br/>Isolated Power Rails, Fourth-Generation Cluster Switching |

The new development board has the Jetson TX1 core mounted in a discovery board with size **17cm x 17 cm**. This board has many connectors from standard PC connection (HDMI, USB, SD, ethernet, etc) and JTAG connection, PCI express, Raspberry bus, etc etc.

{% include figure image_path="assets/review/NVIDIA-jetson-tx1/core_and_carrier_tx1.jpg" alt="Jetson TX1 – core and Carrier" caption="Jetson TX1 – core and Carrier" %}

NVIDIA Jetson TX1 has a continuous voltage supply converter and it works from 5.5V to 19V. In the NVIDIA box contains an AC-DC converter with an output of 19V.

# On board – detail

The Jetson development board has many different connectors. The first one, in the center of this figure, it is mounted with four screws the Jetson TX1 core. Around the TX1 there are many connectors, PCI express for differents expansion boards (example a NVIDIA GTX or audio interface, etc etc). In the corner are mounted four buttons to re-flash the board, control the volume or power on.

In a side the development jetson TX1 board have all PC standard connectors:
* Ethernet
* SD card expansion
* HDMI
* USB3
* USB micro host
* WI-FI plug
* DC power plug

{% include gallery caption="NVIDIA Jetson TX1 parts" %}

More interesting a free space available for expansion board for:
* Camera connector
* Display connection

All GPIO availables can works at 1.8V or 3.3V. This is set with a jumper near the connector.

# Basic information

When Jetson TX1 start, it run with Ubuntu 14.04, in fact if you launch a in command line “lsb_release” you can read all information about the operative system. The Jetson TX1 compare with the Jetson TK1 is more quickly to load all graphical components.
```
$ lsb_release -a
No LSB modules are available.
Distributor ID:    Ubuntu
Description:    Ubuntu 14.04.3 LTS
Release:    14.04
Codename:    trusty
```
When you launch “deviceQuery” on Jetson TX1 you can read all information about the GPU device and other specification about the Tegra X1. In the next quote I’ve copied all information printed.
```
$ ./deviceQuery
./deviceQuery Starting…

CUDA Device Query (Runtime API) version (CUDART static linking)

Detected 1 CUDA Capable device(s)

Device 0: “GM20B”
CUDA Driver Version / Runtime Version          7.0 / 7.0
CUDA Capability Major/Minor version number:    5.3
Total amount of global memory:                 1927 MBytes (2020511744 bytes)
( 2) Multiprocessors, (128) CUDA Cores/MP:     256 CUDA Cores
GPU Max Clock rate:                            72 MHz (0.07 GHz)
Memory Clock rate:                             13 Mhz
Memory Bus Width:                              64-bit
L2 Cache Size:                                 262144 bytes
Maximum Texture Dimension Size (x,y,z)         1D=(65536), 2D=(65536, 65536), 3D=(4096, 4096, 4096)
Maximum Layered 1D Texture Size, (num) layers  1D=(16384), 2048 layers
Maximum Layered 2D Texture Size, (num) layers  2D=(16384, 16384), 2048 layers
Total amount of constant memory:               65536 bytes
Total amount of shared memory per block:       49152 bytes
Total number of registers available per block: 32768
Warp size:                                     32
Maximum number of threads per multiprocessor:  2048
Maximum number of threads per block:           1024
Max dimension size of a thread block (x,y,z): (1024, 1024, 64)
Max dimension size of a grid size    (x,y,z): (2147483647, 65535, 65535)
Maximum memory pitch:                          2147483647 bytes
Texture alignment:                             512 bytes
Concurrent copy and kernel execution:          Yes with 2 copy engine(s)
Run time limit on kernels:                     No
Integrated GPU sharing Host Memory:            Yes
Support host page-locked memory mapping:       Yes
Alignment requirement for Surfaces:            Yes
Device has ECC support:                        Disabled
Device supports Unified Addressing (UVA):      Yes
Device PCI Domain ID / Bus ID / location ID:   0 / 0 / 0
Compute Mode:
< Default (multiple host threads can use ::cudaSetDevice() with device simultaneously) >

deviceQuery, CUDA Driver = CUDART, CUDA Driver Version = 7.0, CUDA Runtime Version = 7.0, NumDevs = 1, Device0 = GM20B
Result = PASS
```

The standard tools is CUDA 7.0 and it work fine.  Follow you can read the NVCC information when you install all graphical drivers.
```
nvcc –version
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2015 NVIDIA Corporation
Built on Mon_Oct__5_15:14:26_CDT_2015
Cuda compilation tools, release 7.0, V7.0.69
```
Finally this is the information about the CPU and the hardware revision.
```
$ cat /proc/cpuinfo
Processor    : Cortex A57 Processor rev 1 (aarch64)
processor    : 0
processor    : 1
processor    : 2
processor    : 3
Features    : fp asimd aes pmull sha1 sha2 crc32 wp half thumb fastmult vfp edsp neon vfpv3 tlsi vfpv4 idiva idivt
CPU implementer    : 0x41
CPU architecture: 8
CPU variant    : 0x1
CPU part    : 0xd07
CPU revision    : 1

Hardware    : jetson_tx1
Revision    : 0000
Serial        : 088403e800000000
```

# Devices

The Jetson TX1 have availables all wi-fi and bluetooth connection with an internal USB connection, in fact when you launch the command “lsusb” you can find a particular device called “Nvidia corp”
```
lsusb
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 003 Device 002: ID 0955:09ff NVidia Corp.
Bus 003 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 002 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
```
This is a printed information about thermal sensors when the Jetson TX1 compile all cuda examples:
```
$ sensors
CPU-therm-virtual-0
Adapter: Virtual device
temp1:        +38.5°C  (crit = +66.0°C)

GPU-therm-virtual-0
Adapter: Virtual device
temp1:        +35.5°C  (crit = +103.0°C)

PLL-therm-virtual-0
Adapter: Virtual device
temp1:        +34.5°C

Tdiode_tegra-virtual-0
Adapter: Virtual device
temp1:        +41.8°C

Tboard_tegra-virtual-0
Adapter: Virtual device
temp1:        +42.0°C

thermal-fan-est.37-virtual-0
Adapter: Virtual device
temp1:        +35.8°C
```