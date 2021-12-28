---
title: "NVIDIA Jetson AGX Xavier"
excerpt: "Jetson AGX Xavier specifications and comparison with other boards"
classes: wide
header:
  teaser: /assets/review/NVIDIA-jetson-AGX-xavier/xavier-structure.png
categories:
  - Review
tags:
  - NVIDIA
  - Jetson
xavier:
  - image_path: "/assets/review/NVIDIA-jetson-AGX-xavier/Bottom.png"
  - image_path: "/assets/review/NVIDIA-jetson-AGX-xavier/ConnectorA.png"
  - image_path: "/assets/review/NVIDIA-jetson-AGX-xavier/ConnectorB.png"
  - image_path: "/assets/review/NVIDIA-jetson-AGX-xavier/DevelopmentKit.png"
---

Yes! I’m excited After the first announcement in the [European GTC17](http://rnext.it/review/gtc-europe-2017/) in Munich last October, yesterday was officially announced the new **NVIDIA Jetson Xavier** the evolution of the [NVIDIA Jetson TX2](http://rnext.it/review/nvidia-jetson-tx2/).

Now are available the new [technical specification](https://developer.nvidia.com/jetson-xavier) about this board, and the [F.A.Q.](https://developer.nvidia.com/embedded/jetson-xavier-faq)


|             | NVIDIA Jetson TX1 | NVIDIA Jetson TX2 | NVIDIA Jetson Xavier |
|-------------|-------------------|-------------------|----------------------|
| **Board**       | 50mm x 87mm<br/>400-pin Samtex SEARAY Compatible Board to Board Connector | 50mm x 87mm<br/>400-pin Samtex SEARAY Compatible Board to Board Connector | 100mm x 87mm with 16mm Z-height<br/>(699-pin board-to-board connector) |
| **Weight** | 85 grams (core) | 85 grams (core) | **??** |
| **CPU** | 4 core 64-bit A57 CPUs | 4core 64-bit and 2 Denver A57 CPUs | 8-core ARMv8.2 64-bit CPU, 8MB L2 + 4MB L3 |
| **GPU** | Maxwell | Pascal | 512-core Volta GPU with Tensor Cores |
| **Storage** | 16 GB eMMC | 32 GB eMMC | 32GB eMMC 5.1 |
| **Memory** | 4 GB 64-bit LPDDR4 25.6 GB/s | 8 GB 128-bit LPDDR4 58.4 GB/s | 16GB 256-bit LPDDR4x - 137 GB/s |
| **Wi-Fi/Bluetooth** | 802.11 2×2 AC/Bluetooth Ready | 802.11 2×2 AC/Bluetooth Ready | No |
| **USB** | (1x) USB 3| | (3x) USB 3.1 (10GT/s)<br/>(4x) USB 2.0 Ports |
| **Video Encode** | 2160p @ 30	| | (2x) 4Kp60 - HEVC |
| **Video Decode** | 2160p @ 30	| 2160p @ 30<br/>12 bit support for H.265, VP9 | (2x) 4Kp60 - 12-bit support |
| **Camera** | 1.4Gpix/s<br/>Up to 1.5Gbps per lane	| 1.4Gpix/s<br/>Up to 2.5Gbps per lane | 16 lanes CSI-2, 40 Gbps in D-PHY V1.2 or 109 GBps in CPHY v1.1<br/>8 lanes SLVS-EC<br/>Up to 16 simultaneous cameras |
| **Power**	| Under 7.5W (Max-Q) | | Three different options:<br/>10W, 15W, 30W |
| **Price** | 300$ | 600$ | 1299$ |

This is a big improvement from the last Jetson TX1 and TX2! From 256 to 512 GPU cores, 8 CPU. More than one USB3 ports in an equivalent of two NVIDIA Jetson TX2 placed side by side. The starting price of this monster is a bit more than a two NVIDIA Jetson TX2.

From the video interview of [armdevices.net](http://armdevices.net/2018/06/04/1299-nvidia-jetson-xavier-dev-kit-8-core-armv8-512-core-volta-gpu-for-ai-robotics/) at Deepu Talla in the last [COMPUTEX 2018](https://www.computextaipei.com.tw/) (A short NVIDIA presentation in [anandtech.com](https://www.anandtech.com/show/12861/computex-2018-nvidia-live-blog-1pm-tw-5am-utc)) we can see a lot of information about Jetson Xavier board.

{% include video id="xaUA_sq4ZJo" provider="youtube" %}

but in particular we can recognize three different type of the same product. In the center the only nacked module, where we can see the same NVIDIA Volta chip (assembled in the DGX) and an extra board with all core of the NVIDIA Jetson; On left the module with the industrial dissipator and medical connector. Finally on right the development kit with the big fan derivation from PC graphics board, and the complete pinout of the board.

{% include gallery id="xavier" caption="NVIDIA Jetson AGX Xavier" %}

The Development kit have a lot of connectors, showed during the interview, but I recognise, if my interpretation is good:

* **A.** GPIO pinout
* **B.** Buttons, maybe: Power on, reset, Firmware reset
* **C.** Camera connector (same of the NVIDIA Jetson TX1/TX2 development kit)
* **D.** Video connector (same of the NVIDIA Jetson TX1/TX2 development kit)
* **E.** Extra pin, maybe the same pins of reset, power on, led, and other
* **F.** MINI-PCI connector
* **G.** –
* **H.** OTG connector
* **I.** USB-C connector
* **J.** –
* **K.** –
* **L.** HDMI connector
* **M.** eSATA/USB3 hybrid port connector
* **N.** Ethernet connector
* **O.** Power plug connector
* **P.** PCIe connector

{% include figure image_path="/assets/review/NVIDIA-jetson-AGX-xavier/JetsonXavier-Version.png" alt="NVIDIA Jetson AGX Xavier versions" caption="NVIDIA Jetson AGX Xavier versions" %}

NVIDIA provides a suite of software products for the simulation, training, verification and deployment of Jetson Xavier — consisting of:

* **Isaac SDK** – a collection of APIs and tools to develop robotics algorithm software and runtime framework with fully accelerated libraries.
* **Isaac IMX** – Isaac Intelligent Machine Acceleration applications, a collection of NVIDIA-developed robotics algorithm software.
* **Isaac Sim** – a highly realistic virtual simulation environment for developers to train autonomous machines and perform hardware-in-the-loop testing with Jetson Xavier.

I’m curious to test the new NVIDIA Jetson Xavier on my robot!