---
title: "jetson-easy"
excerpt: ":nut_and_bolt: Automatically script to setup and configure your NVIDIA Jetson [Nano, Xavier, TX2i, TX2, TX1, TK1] . This script run different modules to update, fix and patch the kernel, install ROS and other..."
classes: wide
number: 2016
link: https://github.com/rbonghi/jetson_easy
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/project/jetson-easy/jetson-easy_header.png
  teaser: /assets/project/jetson-easy/jeson-easy.jpg
  actions:
    - label: "Github"
      url: "https://github.com/rbonghi/jetson_easy"
---

The idea of this project is automatically update and setup your [NVIDIA Jetson][NVIDIA Jetson] [Nano, Xavier, TX2i, TX2, TX1, TK1] embedded board without wait a lot of time.

Main features:
* [**Biddibi Boddibi Boo**](#biddibi-boddibi-boo) is an automatic and **REMOTE** NVIDIA Jetson installer, from update&upgrade, patch the kernel or install [ROS][ROS]
* The [**Jetson_performance**](#jetson_performance-jetson_variables-and-jetson_release) is a service to control the performance of the board, [**jetson_variables**](#jetson_performance-jetson_variables-and-jetson_release) add new environments variables and [**jetson_release**](#jetson_performance-jetson_variables-and-jetson_release) show the information about the board.

If you want start with this toolkit you can write in your server bash:
```console
ubuntu@server:~$ git clone https://github.com/rbonghi/jetson_easy.git
ubuntu@server:~$ cd jetson_easy
ubuntu@server:~/jetson_easy$ ./biddibi_boddibi_boo.sh
```

Follow the direct link: