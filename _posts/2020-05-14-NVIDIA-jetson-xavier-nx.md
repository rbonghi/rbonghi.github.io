---
title: "NVIDIA Jetson Xavier NX"
excerpt: "NVIDIA Jetson Xavier NX is the newest addition to the Jetson platform, delivering high performance in a very small form factor and power envelope, and it is not a substitution of the previous Jetson Nano in only 80mm x 100mm."
header:
  teaser: /assets/review/NVIDIA-jetson-xavier-nx/xavierNX.jpg
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
  - url: /assets/review/NVIDIA-jetson-xavier-nx/difference_packages.jpg
    image_path: /assets/review/NVIDIA-jetson-xavier-nx/difference_packages.jpg
    alt: "Size packages"
    title: "Size packages"
  - url: /assets/review/NVIDIA-jetson-xavier-nx/difference_packages_2.jpg
    image_path: /assets/review/NVIDIA-jetson-xavier-nx/difference_packages_2.jpg
    alt: "Side packages"
    title: "Side packages"
board:
  - url: /assets/review/NVIDIA-jetson-xavier-nx/XavierNX-top.jpg
    image_path: /assets/review/NVIDIA-jetson-xavier-nx/XavierNX-top.jpg
    alt: "NVIDIA Jetson Xavier NX - Top"
    title: "NVIDIA Jetson Xavier NX - Top"
  - url: /assets/review/NVIDIA-jetson-xavier-nx/XavierNX-botton.jpg
    image_path: /assets/review/NVIDIA-jetson-xavier-nx/XavierNX-botton.jpg
    alt: "NVIDIA Jetson Xavier NX - Botton"
    title: "NVIDIA Jetson Xavier NX - Botton"
code_name:
  - url: /assets/review/NVIDIA-jetson-xavier-nx/Porg.jpg
    image_path: /assets/review/NVIDIA-jetson-xavier-nx/Porg.jpg
    alt: "Porg"
    title: "Porg"
  - url: /assets/review/NVIDIA-jetson-xavier-nx/Jakku.jpg
    image_path: /assets/review/NVIDIA-jetson-xavier-nx/Jakku.jpg
    alt: "Jakku"
    title: "Jakku"
---
A new Jetson is here! Last year NVIDIA release the first Jetson in a new System on Module (SoM) package. Compare the other NVIDIA Jetson has a compact form factor and it is simple to make a homemade carrier.

![NVIDIA Jetson Xavier NX Package](xaviernx-box.jpg)

NVIDIA Jetson Xavier NX is the newest addition to the Jetson platform, delivering high performance in a very small form factor and power envelope, and it is not a substitution of the previous Jetson Nano.

NVIDIA Jetson Xavier NX, based on the ground-breaking NVIDIA Volta GPU architecture with 384 CUDA cores, 48 Tensor cores, and 2 Deep Learning Accelerator (DLA) engines, brings supercomputer-class performance to edge applications in an ultra-compact, credit card sized System-on-Module. Jetson Xavier NX delivers 21 Trillion Operations per Second (TOPS) of deep learning performance at under 15 Watts of power and is backed by the comprehensive NVIDIA Artificial Intelligence and Deep Learning software stack.

The new NVIDIA Jetson Xavier NX deliver the following key benefits to edge AI devices:
* Brings Cloud-Native Computing to Edge AI Devices
* Complete AI Platform
* One Platform for Multiple Edge Applications
* Seamless and Rapid Development Experience
* Fast Time-to-Market

**The Jetson Xavier NX Developer Kit is now available for *$399* at [NVIDIA.com](https://nvda.ws/3bqcNEx) and from channel partners worldwide. But now hands on this new developer kit!** 

# Package and unboxing

When you bring your box, the first difference that I notice is the box size. I bigger than the Jetson Nano package, and compare the Jetson Nano is included a Power supply to switch on the NVIDIA Jetson Xavier NX. In particular in the second picture is listed all components included.

{% include gallery caption="Difference between Jetson Xavier NX package and Jetson Nano 4gb package" %}

The feeling when you open the new box is to have something bigger compare the other boards, and like the previous package.

![Inside the NVIDIA Jetson Xavier NX box](inside_box.jpg)

Inside the box is included a **45W Power Supply Unit** (PSU) and works at **19V**.

Yes compare the NVIDIA Jetson Nano, the new NVIDIA Jetson Xavier NX require 19V at 2.3A to works! To control more power the new Jetson Xavier NX require more POWER! I will go more in deep about the power supply on the next chapter.

# Hardware and Design

The new look of the **Jetson Xavier NX** is similar to the previous Jetson Nano, but there are some new parts just leap out at you. The first one is FINALLY a new integrated fan on the dissipator. I love this new engineering choice for this developer board! Now when I will use on my robots I will not count an extra space for the fan. It’s a compact board with all I needed.

Second point the new NVIDIA Jetson Xavier NX have a new black stand, where compare the Jetson Nano make at this developer kit a nice look and safe better all pins and other components behind the carrier.

{% include gallery id="board" caption="Difference between Jetson Xavier NX package and Jetson Nano 4gb package" %}

On bottom the carrier is completely different compare the Jetson Nano developer kits. Finally we have a simple space to mount the Wireless M.2 module card and in the same time mount a NVMe SSD board.

A great point for the new Jetson Xavier NX developer kit is included a WiFi module with antennas, and we can see already mounted on the bottom of the board.

## Architecture

The NVIDIA Jetson Xavier NX is born from a the [NVIDIA Volta Architecture](https://www.nvidia.com/en-gb/data-center/volta-gpu-architecture/) with 384 NVIDIA CUDA cores plus 48 Tensor cores! A new evolution from a Maxwell 128-core on Jetson Nano. The CPU architecture works on a 6 core [ARMv8.2](https://community.arm.com/developer/ip-products/processors/b/processors-ip-blog/posts/armv8-a-architecture-evolution) at 64bit and use 2 NVLDA engines plus 8GB RAM DDR4.

![Hardware design](900px-Jetson_NX_Block_Diagram.png)

A deep table with all specification is below:

| Feature | Specifications |
|---------|----------------|
| Power mode | 10W (Max efficiency) - 15W (Max performance) |
| GPU | NVIDIA Volta architecture with 384 NVIDIA CUDA® cores and 48 Tensor cores |
| CPU | 6-core NVIDIA Carmel ARM®v8.2 64-bit CPU 6 MB L2 + 4 MB L3 |
| DLA | 2x NVDLA Engines |
| Memory | 8 GB 128-bit LPDDR4x @ 51.2GB/s |
| Storage | microSD (card not included) |
| Video Encode | 2x 4K @ 30 - 6x 1080p @ 60 - 14x 1080p @ 30 (H.265/H.264) |
| Video Decoder | 2x 4K @ 60 - 4x 4K @ 30 - 12x 1080p @ 60 - 32x 1080p @ 30 (H.265)<br/>2x 4K @ 30 - 6x 1080p @ 60 - 16x 1080p @ 30 (H.264) |
| Camera | 2x MIPI CSI-2 DPHY lanes|
| Connectivity | Gigabit Ethernet, M.2 Key E (WiFi/BT included), M.2 Key M (NVMe)|
| Display Connectors | HDMI and DP|
| USB | 4x USB 3.1, USB 2.0 Micro-B|
| Mechanical | 103 mm x 90.5 mm x 31 mm|

The NVIDIA Jetson Xavier NX have 5 NVP models where you can setup your separated in two macro categories

| 10W (Max efficiency) | 15W (Max performance)|
|----------------------|----------------------|
|MODE_10W_2CORE | MODE_15W_2CORE|
|MODE_10W_4CORE | MODE_15W_4CORE|
| | MODE_15W_6CORE|

Below a screen from jtop

![jtop NVIDIA Jetson Xavier NX](jtop-xaviernx.png)

Now jetson-stats works with jetson Xavier NX, install with:
```
sudo -H pip install -U jetson-stats
```

For each NVP model we have different CPU clock configuration

| | NVP model | With Jetson Clocks |
|-|-----------|--------------------|
|0 | **MODE_15W_2CORE** | 1.2-1.9Ghz	1.9Ghz
|1 | **MODE_15W_4CORE** | 1.2-1.4Ghz	1.4Ghz
|2 | **MODE_15W_6CORE** | 1.2-1.4Ghz	1.4Ghz
|3 | **MODE_10W_2CORE** | 1.2-1.5Ghz	1.5Ghz
|4 | **MODE_10W_4CORE** | 1.2Ghz	1.2Ghz

The GPU and EMC frequencies change using Jetson Clocks

|     | Without Jetson Clocks	10W | Jetson Clocks	15W | Jetson Clocks |
|-----|---------------------------|-------------------|---------------|
| **GPU** | 114Mhz | 803Mhz | 1.1Ghz
| **EMC** | 204Mhz | 1.6Ghz | 1.6Ghz

Finally the default memory configuration use 6 ZRAM slot at 500Mb. Below a screenshot from jtop

![jtop memory - NVIDIA Jetson Xavier NX](jetson-xaviernx-mem.png)

## Difference between Jetson Nano

Like what I show before, the Jetson Xavier NX have a similar carrier of the Jetson Nano.

**ATTENTION!** You can use the Xaver NX module only with the Carrier, but please follow this notes on: [Considerations when using Jetson Xavier NX module with Nano devkit carrier](https://forums.developer.nvidia.com/t/considerations-when-using-jetson-xavier-nx-module-with-nano-devkit-carrier/119786)
{: .notice--warning}

There are some interesting differences:

| Jetson Nano | Jetson Xavier NX |
|-------------|------------------|
|Dissipator fanless | Dissipator with fan
|5V – Max 4A | 19V – Max 5A
|No Wifi module | WiFi module M.2 on kit
|Power supply from Micro USB | –
|– | NVMe SSD connector

|[Jetson Nano and Jetson Xavier NX Developer kit](jetson-nano-jetson-xaviernx.jpg)

Another interesting note is the Code Name evolution, we are following the names of actors or plants in last  Star Wars trilogy. Yes is silly, but NVIDIA engineers for this family of board use characters in Star Wars! 🙂 

{% include gallery id="code_name" caption="Star Wars code names **Porg** and **Jakku**" %}

Porg were a species of sea-dwelling bird. They were native to the planet Ahch-To, where Jedi Master Luke Skywalker made his exile in the years prior to the Battle of Crait. More info from [Wookiepedia](https://starwars.fandom.com/wiki/Porg)

This board have the same name of the scavenger Rey home world in Star wars. Who became involved in the events of the cold war after helping the former First Order stormtrooper Finn and the astromech droid BB-8 escape offworld with a map leading to the missing Jedi Luke Skywalker. More info from [Wookiepedia](https://starwars.fandom.com/wiki/Jakku)

![jtop architecture and libraries](jtop-info-xaviernx.png)

# Cloud Native Architecture

Cloud-native technologies are the way forward: microservice architecture, containerization, and orchestration have enabled cloud applications to escape the constraints of older, monolithic software workflows. A similar transformation is now coming to AI edge devices. The jump to microservice
architecture results in the split of applications into collections of small services. Because development of a self-contained service can be done without necessarily having to update other application components, time to market can be accelerated with scalable software development, and updates throughout the product life cycle are made easier.

![Cloud Native on NVIDIA Jetson Xavier NX](XavierNX_cloud_native.gif)

The use of containerized applications brings cloud-native capability to edge devices. Packaging application components and their dependencies together in containers for deployment allows clear separation between an application and the underlying software environment. This enables OS updates for feature enhancements or bug/security fixes without impacting installed applications, and vice versa.
Applications can be installed, updated, rolled back, or removed without impacting the OS.

# Multicontainers

First test that I run is the multicontainer demo, this is built around the example use case of AI applications for service robots. Service robots are autonomous robots and interact with people usually in retail, hospitality, healthcare, or warehouse settings.
Consider a service robot in a retail setting providing customer service, like interacting with customers and providing helpful answers to customer queries.

These robots need to perform the following tasks:
* Identify humans
* Detect when a customer is talking to it
* Understand where a customer is pointing to while interacting with it
* Understand what a customer is asking
* Provide useful answers.

Hence these robots needs multiple AI models such as:
* People identification to identify humans
* Gaze detection to detect when a customer is talking to it (as opposed to talking to someone else)
* Pose detection to detect customer’s pose
* Speech recognition to detect words in sentences spoken by the customer
* Natural language processing to understand the sentence, including context, to provide relevant answers back to the customer.

The demo runs seven models simultaneously as described below:

* DeepStream Container with people detection:
  * **Resnet-18 model** with input image size of 960X544X3. The model was converted from **TensorFlow** to **TensorRT**.
* Pose container with pose detection:
  * **Resnet-18 model** with input image resolution of 224X224. The model was converted from **PyTorch** to **TensorRT**.
* Gaze container with gaze container:
  * **MTCNN model** for face detection with input image resolution of 260X135. The model was converted from **Caffe** to **TensorRT**.
  * **NVIDIA Facial landmarks model** with input resolution of 80X80 per face. The model was converted from **TensorFlow** to **TensorRT**.
  * **NVIDIA Gaze model** with input resolution of 224X224 per left eye, right eye and whole face. The model was converted from **TensorFlow** to **TensorRT**.
* Voice container with speech recognition and Natural Language Processing:
  * **Quartznet-15X5 model** for speech recognition which was converted from **PyTorch** to **TensorRT**.
  * **BERT Base model** for language model for NLP which was converted from **TensorFlow** to **TensorRT**.

![Multi container demo](CloudNativeScreenshot.png)

The output is literally amazing! In four quadrants I can see in real time:
* People detection container
* Natural Language Processing Container
* Pose estimation
* Gaze Estimation

![Docker images](docker_images.png)

![Docker containers](docker_containers.png)

There are five containers in action on Jetson Xavier NX:
* Deepstream-mcdemo
* jetson-voice
* pose-demo
* gaze-demo
* deepstream-demo-pretrained

## Jetson Xavier NX a AI platform

The NVIDIA AI platform brings optimized AI tools, libraries, and SDKs such
as CUDA, CuDNN, TensorRT, and DeepStream to the Jetson platform, enabling developers to seamlessly train AI applications on powerful cloud GPUs and deploy trained networks on Jetson-powered AI edge devices.

All libraries and SDK are simple to install directly from the SDK manager and with Jetpack now (OTA) update a Jetson board is really simple! 

![Deep Learning Inference Performance](DeepLearningInferencePerformance.png)

# Benchmark

Last test is check the performance of the new NVIDIA Jetson Xavier NX, to test it, I use this really cool benchmark repository [jetson_benchmark](https://github.com/NVIDIA-AI-IOT/jetson_benchmarks) where is possible to test different models directly on board. the output is completely another story compare a Nano. In the same size another power!

| Model Name | FPS<br/>Jetson Nano | FPS<br/>Jetson Xavier NX <br/>15W 2 Core<br/>With Jetson Clocks | FPS<br/>Jetson Xavier NX<br/>15W 6 core<br/>With Jetson Clocks |
|-----|---------|------|------|
|0 inception_v4 | 10.631948 | 316.895566 | 316.478577 |
|1 vgg19_N2 | 7.692173 | 65.424157 | 63.582191 |
|2 super_resolution_bsd500 | 10.704373 | 152.186116 | 159.201983 |
|3 unet-segmentation | 11.502981 | 144.152678 | 144.005892 |
|4 pose_estimation | 10.191128 | 234.183907 | 235.400592 |
|5 yolov3-tiny-416 | 33.927461 | 570.071398 | 589.816623 |
|6 ResNet50_224x224 | 25.933791 | 845.337518 | 830.919699 |
|7 ssd-mobilenet-v1 | 29.884008 | 884.193146 | 894.364623 |

# Price and shop

The Jetson Xavier NX Developer Kit is now available for **$399** at [NVIDIA.com](https://nvda.ws/3bqcNEx) and from channel partners worldwide.
{: .notice--success}

![NVIDIA Jetson Xavier NX](xaviernx-shop.png)