---
title: "ROS jetson stats"
excerpt: ":turtle: An plugin of ROS web console to interact the robot in an augmented reality environment. With this robot you can draw in real-time a new wall or clean an area with your phone or tablet. This application require another rosnode to fuse the information from the virtual world and real world."
permalink: /project/ros_jetson_stats/
classes: wide
number: 2019
link: https://github.com/rbonghi/ros_jetson_stats
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: https://github.com/rbonghi/ros_jetson_stats/raw/master/.github/runtime_monitor.gif
  teaser: https://github.com/rbonghi/ros_jetson_stats/raw/master/.github/runtime_monitor.gif
  actions:
    - label: "Repository"
      url: "https://github.com/rbonghi/ros_jetson_stats"
---

A ROS wrapper [jetson-stats](https://github.com/rbonghi/jetson_stats) to ROS where you can read the status of your board via diagnostic messages.

# Installation

1. Check your NVIDIA board have installed jetson-stats otherwise install it
```elm
sudo -H pip install -U jetson-stats
```
2. Clone this repository in your workspace
3. Run catkin_make to locate `ros_jetson_stats` in your workspace

## Setup your launch file

Add in your launch file the `ros_jetson_stats` package following
```xml
<node pkg="ros_jetson_stats" type="jetson_stats.py" name="ros_jetson_stats"/>
```