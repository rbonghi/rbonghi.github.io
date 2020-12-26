---
title: "NVIDIA Jetson TX2"
excerpt: "A full review of the NVIDIA Jetson TX2. The first feeling with the new embedded board built from NVIDIA, the successor of Jetson TX1."
header:
  teaser: /review/NVIDIA-jetson-tx2/jetsonTX2.jpg
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
  - url: /review/NVIDIA-jetson-tx2/GPIOExpansionHeader1.png
    image_path: /review/NVIDIA-jetson-tx2/GPIOExpansionHeader1.png
    alt: "GPIO Expansion Header 1"
    title: "GPIO Expansion Header 1"
  - url: /review/NVIDIA-jetson-tx2/GPIOExpansionHeader2.png
    image_path: /review/NVIDIA-jetson-tx2/GPIOExpansionHeader2.png
    alt: "GPIO Expansion Header 2"
    title: "GPIO Expansion Header 2"
---

The new Jetson TX2 is here! After one year the NVIDIA show a new version of the TX family embedded board.

From the experience with the [NVIDIA Jetson TX1](/review/NVIDIA-jetson-tx1) the [NVIDIA](http://www.nvidia.com/) does not change the form factor and the pinout with the Jetson TX1, but improve the electronic characteristic and the software release, following the evolution of the graphic cards 10xx announced on 6th May and released on 27th May, 2016 use the new Pascal GPU the new Jetson TX2 use the new GPU Pascal.

With the Jetson TX2 we can start to work with the ubuntu kernel 4.4 and now the CUDA 8.0 has working with the Jetson TX2, and with four CPUs and other two Denver CPUs the new Jetson TX2 can start to improve your experience in robotics and automotive.

# Hardware design

The hardware of the Jetson TX2 working with 256 CUDA core at 1.3Ghz, a bit speed up compare the Jetson TX1 (256 CUDA core at 72Mhz). The new architecture with codename Pascal, successor of Maxwell family working with a doubled L2 cache size 524288 bytes.

![The length of the Jetson TX2 is the same of a AAA battery](NVIDIA_JetsonTX2_battery_module_WHT_2000pxWM.png)

Compare with the NVIDIA Jetson TX1 the new NVIDIA Jetson TX2 now use 8 GB 128 bit of memory with a doubled velocity of connection. You have a new feeling when you launch an application, an enhanced velocity of response. The same Board to board connector, the [Samtex SEARAY](https://www.samtec.com/connectors/high-speed-board-to-board/high-density-arrays/searay) 400 pin, allow to use the same designed connectors with the new Jetson TX2 all possessorsof Jetson [Elroy carriers](http://www.connecttech.com/) can breathe a sigh of relief.

In the following table are collected all principal electronic and mechanical characteristic

| | NVIDIA Jetson TX1 | NVIDIA Jetson TX2 |
|-|-------------------|-------------------|
| Board	| 50mm x 87mm<br/>400-pin Samtex SEARAY Compatible Board to Board Connector
| Weight | 85 grams (core)
| CPU | 4 core 64-bit A57 CPUs | 4core 64-bit and 2 Denver A57 CPUs
| GPU | Maxwell | Pascal
| Storage | 16 GB eMMC | 32 GB eMMC
| Memory | 4 GB 64-bit LPDDR4 25.6 GB/s | 8 GB 128-bit LPDDR4 58.4 GB/s
| Wi-Fi/Bluetooth | 802.11 2×2 AC/Bluetooth Ready |
| Video Encode | 2160p @ 30 |
| Video Decode | 2160p @ 30 | 2160p @ 30<br/>12 bit support for H.265, VP9 |
| Camera	1.4Gpix/s<br/>Up to 1.5Gbps per lane | 1.4Gpix/s<br/>Up to 2.5Gbps per lane |
| Power | Under 7.5W (Max-Q) |
 
About the electronics interface the NVIDIA have increased the number of I2C interface and **finally** have introduced the the CAN bus hardware interface, a speed up in industrial and automotive fields where is required this interface to connect sensors, actuators and other devices.

|  | NVIDIA Jetson TX1 | NVIDIA Jetson TX2 |
|---|---|---|
| USB | 3x USB 2.0 and up to 3x USB 3.0 |
| PCIe | 1×4 + 1×1 | Up to 1×4 + 1×1 or 2×1 + 1×2 |
| SATA | Yes | Yes (with device sleep option) |
| Camera | CSI: 6×2 or 3×4 - MCLK: 2x | CSI: 6×2 or 3×4 - MCLK: 4x |
| Display | **eDP/DP/HDMI**: 2x(HDMI on DP1 only)<br/>**DSI**: 2×4<br/>Blacklight PWM: 1x<br/>**GSYNC_HSYNC/VSYNC**: Not Available | **eDP/DP/HDMI**: 2x(Symmetrical – eDP/DP/HDMI on either DP0 or DP1)<br/>**DSI**: 2×4 (with split link option)<br/>**Blacklight PWM**: 2x<br/>**GSYNC_HSYNC/VSYNC**: Supported |
| Audio | **I2S**: 4x<br/>**Digital Mic**: Not available<br/>**Digital Speaker**: Non available | **I2S**: 4x<br/>Digital **Mic**: Supported<br/>**Digital Speaker**: Supported |
| SDMMC | SD Card + SDIO | SD Card **OR** SDIO |
| Gigabit Ethernet | Supported |
| I2C | 3x | 5x |
| SPI | 3x |
| CAN | Not available | 2x |

# Unboxing

Inside the box Jetson box, have:
* NVIDIA Jetson TX2
* Carrier for NVIDIA Jetston TX2
* Camera module
* USB micro connector
* USB host adaptor
* 2 antennas
* Power supply
* Connector

Compare with the Jetson TX1, the box of NVIDIA Jetson TX2 have the same accessories, and the power supply is the same of the Jetson TX1. In the next picture we can not see any difference. These produce the same output current at the same voltage: 19V at 4.74A – 90W.

![Comparison between power supply of Jetson TX1 and Jetson TX2](comparison_power_supply.jpg)

About the carrier of Jetson TX2 we can see the the same look of the Jetson TX1, just some LEDs are in plus. These LEDs show the status of PCIe port, the status of Jetson TX2 and the power supply.

![The Jetson TX2](JetsonTX2_overview.jpg)

The carrier have the size 17mm x 17mm and the position of the screw layout is the same of an ITX board.

![Screw layout carrier Jetson TX2](carrier_layout.jpg)

The carrier of TX2 have same connectors of the before Jetson TX1, fixed in the same place of the board:
* Ethernet
* SD card expansion
* HDMI
* USB3
* USB micro host
* WI-FI plug
* DC power plug
* PCIe x4 connector
* SATA port

Other for test:
* Debug UART1
* JTAG
* 2 GPIO Extension header
* Display expansion header
* Camera expansion header
* Charge header
* GPIO and buttons (Reset, power, volume down, Recovery)

{% include gallery caption="GPIO Expansion Header" %}

# Software

With the new release of Jetson the NVIDIA team released the new linux kernel 4.4 and use all last released code to work with the GPU.

| Version | Component |
|---|---|
| Linux | Ubuntu 16.04 LTS |
| Kernel | 4.4 |
| OpenGL/ES/EGL | 4.5/3.2/1.4 |
| Vulkan | 1.0.3 |
| Multimedia API | 27.1 |
| libargus camera | 0.95 |
| CUDA | 8.0.64 |
| Tensor RT | 1.0 GA |
| CuDNN | 5.1 |
| Visionworks | 1.6 |
| OpenCV4Tegra | 2.4.13 |

Now the NVIDIA Jetson TX2 is integrated on the new Jetpack 3.0. This SDK have integrated all library for Artificial Intelligence and robotics, with the new release you can download in your Jetson [ROS](http://wiki.ros.org/) and other famous library for vision.

# Test with the Jetson TX2

The Jetson TX2 start with Ubuntu 16.04 LTS with the registered user “nvidia” pass: “nvidia” and the default system user in “ubuntu” pass: “ubuntu”. In the second user are available all demo folders to try the performance of the CUDA core Pascal architecture and other demos about the camera. In the ubuntu home folder there are all CUDA libraries, visionworks CuDNN and other.

But the first test after the first wake-up is to check which release of Ubuntu is installed inside, in command line we can launch the “lsb_release” to read all information about the operative system.
```
ubuntu@tegra-ubuntu$: lsb_release -a
No LSB modules are available.
Distributor ID: Ubuntu
Description: Ubuntu 16.04.2 LTS
Release: 16.04
Codename: xenial
```
Another check is execute the “deviceQuery” process placed in the CUDA example folder and read the status of the GPU, and compare with the Jetson TX1 it start with CUDA release 8.0
```
ubuntu@tegra-ubuntu:~/NVIDIA_CUDA-8.0_Samples/1_Utilities/deviceQuery$ ./deviceQuery
./deviceQuery Starting…

CUDA Device Query (Runtime API) version (CUDART static linking)

Detected 1 CUDA Capable device(s)

Device 0: “GP10B”
CUDA Driver Version / Runtime Version 8.5 / 8.0
CUDA Capability Major/Minor version number: 6.2
Total amount of global memory: 7853 MBytes (8234323968 bytes)
( 2) Multiprocessors, (128) CUDA Cores/MP: 256 CUDA Cores
GPU Max Clock rate: 1301 MHz (1.30 GHz)
Memory Clock rate: 13 Mhz
Memory Bus Width: 64-bit
L2 Cache Size: 524288 bytes
Maximum Texture Dimension Size (x,y,z) 1D=(131072), 2D=(131072, 65536), 3D=(16384, 16384, 16384)
Maximum Layered 1D Texture Size, (num) layers 1D=(32768), 2048 layers
Maximum Layered 2D Texture Size, (num) layers 2D=(32768, 32768), 2048 layers
Total amount of constant memory: 65536 bytes
Total amount of shared memory per block: 49152 bytes
Total number of registers available per block: 32768
Warp size: 32
Maximum number of threads per multiprocessor: 2048
Maximum number of threads per block: 1024
Max dimension size of a thread block (x,y,z): (1024, 1024, 64)
Max dimension size of a grid size (x,y,z): (2147483647, 65535, 65535)
Maximum memory pitch: 2147483647 bytes
Texture alignment: 512 bytes
Concurrent copy and kernel execution: Yes with 1 copy engine(s)
Run time limit on kernels: No
Integrated GPU sharing Host Memory: Yes
Support host page-locked memory mapping: Yes
Alignment requirement for Surfaces: Yes
Device has ECC support: Disabled
Device supports Unified Addressing (UVA): Yes
Device PCI Domain ID / Bus ID / location ID: 0 / 0 / 0
Compute Mode:
< Default (multiple host threads can use ::cudaSetDevice() with device simultaneously) >

deviceQuery, CUDA Driver = CUDART, CUDA Driver Version = 8.5, CUDA Runtime Version = 8.0, NumDevs = 1, Device0 = GP10B
Result = PASS
```
Follow you can read the NVCC information when you install all graphical drivers.
```
ubuntu@tegra-ubuntu:$ nvcc –version
nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2016 NVIDIA Corporation
Built on Mon_Jan_23_12:28:25_CST_2017
Cuda compilation tools, release 8.0, V8.0.62
```
Finally this is the information about the CPU and the hardware revision.
```
ubuntu@tegra-ubuntu:~$ cat /proc/cpuinfo
processor : 0
model name : ARMv8 Processor rev 3 (v8l)
BogoMIPS : 62.50
Features : fp asimd evtstrm aes pmull sha1 sha2 crc32
CPU implementer : 0x41
CPU architecture: 8
CPU variant : 0x1
CPU part : 0xd07
CPU revision : 3

….
….
….
```
The processors 0, 3, 4 and 5 have the same informations.

# Temperature test

With this test has checked the performance of the NVIDIA Jetson TX2 to launch the example particles with and without the jetson-clock script. On top we can see the temperature inside the Jetson TX2

{% include video id="Sq6-94ZWK4c" provider="youtube" %}