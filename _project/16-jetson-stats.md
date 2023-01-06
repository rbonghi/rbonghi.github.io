---
title: "jetson-stats"
excerpt: "📊 Simple package for monitoring and control your NVIDIA Jetson [Orin, Xavier, Nano, TX] series"
permalink: /project/jetson-stats/
classes: wide
number: 2018
link: https://github.com/rbonghi/jetson_stats
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/project/jetson-stats/jtop_header.png
  teaser: /assets/project/jetson-stats/jtop.gif
  actions:
    - label: ":sparkling_heart: Sponsor"
      url: "https://github.com/sponsors/rbonghi"
    - label: "Github"
      url: "https://github.com/rbonghi/jetson_stats"
    - label: "Documentation"
      url: "https://rnext.it/jetson_stats/"
---

[![PyPI - Downloads](https://img.shields.io/pypi/dw/jetson-stats.svg)](https://pypistats.org/packages/jetson-stats) [![PyPI version](https://badge.fury.io/py/jetson-stats.svg)](https://badge.fury.io/py/jetson-stats) [![PyPI - Python Version](https://img.shields.io/pypi/pyversions/jetson-stats.svg)](https://www.python.org/) [![PyPI - Format](https://img.shields.io/pypi/format/jetson-stats.svg)](https://pypi.org/project/jetson-stats/) [![GitHub](https://img.shields.io/github/license/rbonghi/jetson_stats)](/LICENSE) [![Docker Pulls](https://img.shields.io/docker/pulls/rbonghi/jetson_stats)](https://hub.docker.com/r/rbonghi/jetson_stats) [![CI & CD](https://github.com/rbonghi/jetson_stats/workflows/CI%20&%20CD/badge.svg)](https://github.com/rbonghi/jetson_stats/actions?query=workflow%3A%22CI+%26+CD%22)

**jetson-stats** is a package for **monitoring** and **control** your [NVIDIA Jetson][NVIDIA Jetson] [Orin, Xavier, Nano, TX] series. Works with all NVIDIA Jetson ecosystem.

![jtop](https://github.com/rbonghi/jetson_stats/wiki/images/jtop.gif)

# Install

```console
sudo -H pip3 install -U jetson-stats
```
**🚀 That's it! 🚀** 

_PS: Don't forget to **reboot** your board_

**You can run jtop in your python script [read here][library]**

## Virtual environment

If you need to install in a virtual environment like *virtualenv*, you **must** install before in your host **and after** in your environment, like:
```
virtualenv venv
source venv/bin/activate
pip install -U jetson-stats
```

## Docker

You can run jtop from a docker container, but you **must** install jetsons-stats as well on your host! Try with the command below:
```console
docker run --rm -it -v /run/jtop.sock:/run/jtop.sock rbonghi/jetson_stats:latest
```

or you can add in your Dockerfile writing:

```docker
FROM python:3-buster
RUN pip install -U jetson-stats
```


[NVIDIA Jetson]: https://developer.nvidia.com/buy-jetson
