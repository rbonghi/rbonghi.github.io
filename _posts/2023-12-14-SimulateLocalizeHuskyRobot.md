---
title: "Simulate and Localize a Husky Robot with NVIDIA Isaac"
excerpt: "How to use Husky robot on NVIDIA Isaac SIM and Isaac ROS"
classes: wide
link: https://developer.nvidia.com/blog/simulate-and-localize-a-husky-robot-with-nvidia-isaac/
header:
  teaser: /assets/posts/NVIDIA/isaac-robotics-clearpath-husky-robot.jpg
categories:
  - Publications
tags:
  - Blog
---

The Husky robot, developed by Clearpath Robotics, is a versatile four-wheeled platform made for indoor and outdoor research use. It is simple to modify by adding other sensors and changing the high-level board. This post explains how to use the official ROS 2 Husky packages to import the robot into NVIDIA Isaac Sim and create a simulation.

For this demo, the Husky robot is equipped with an NVIDIA Jetson Orin Nano and a ZED 2 camera mounted on top. Driving the Husky uses the latest version of Isaac ROS 2, which includes Isaac ROS packages for robot localization (NVIDIA Isaac ROS VSLAM), map building (NVIDIA Isaac ROS NvBlox), and Apriltag detection (NVIDIA Isaac ROS AprilTag). 