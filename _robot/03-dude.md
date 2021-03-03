---
title: "Dude"
excerpt: "For Unmanned Discovering of Enviroments"
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
toc_sticky: true
number: 2014
header:
  teaser: /assets/robot/dude/dude.jpg
  overlay_image: /assets/robot/dude/dude_header.jpg
slam:
  - url: /assets/robot/dude/SLAM-1.jpg
    image_path: /assets/robot/dude/SLAM-1.jpg
    alt: "Flap and power bank holder orientation"
    title: "Flap and power bank holder orientation"
  - url: /assets/robot/dude/SLAM-2.jpg
    image_path: /assets/robot/dude/SLAM-2.jpg
    alt: "Flap and power bank holder slicer support type tree"
    title: "Flap and power bank holder slicer support type tree"
---

Dude is a little robot for with two wheels (diameter 7cm and 14cm of wheelbase) and weight about 2 kg. It is equipped by a RGBD sensor, a NVIDIA Jetson TK1 board and the unav motor control board. This robot interact and perceives of obstacles around it. it can send real time all pictures from the environment that surrounds it. The applications for "Dude" are wandering and interaction with humans in unknown environments, you study of intelligent control techniques for human-computer interaction, the children's entertainment, etc etc.

# Autonomous

{% include video id="AwjWyYiNe6I" provider="youtube" %}

With ROS, Dude can wandering autonomously and with a web remote control you can read all telemetry information and diagnostic the heat of  the robot. The sensors of the robot are RGBD camera and encoder for the wheels.

# SLAM

{% include video id="9xmIucDrj4c" provider="youtube" %}

Simultaneous Localization And Mapping (SLAM) is used for dude robot to localize and mapping an unknown area. This process consists of a number of steps, filtering the information from different sensors, estimate the position with cameras, re observing the environment robot moves around and updating where the robot thinks it is based on these features.

{% include gallery id="slam" caption="Dude SLAM" %}

# Interaction

{% include video id="A2wEXfcD7Sg" provider="youtube" %}

With the SLAM and an high level control dude can interact with the environment. A graphic interface for PC or an web remote control  system. You can set a goal inside a map, built in real time, and you can see the robot build a path and following it.

# Open source & open hardware

It's totally available the source code to configure my same robot.

On my github account you can download all code and the mechanical design of the robot.

Follow the special feature available in this robot.