---
title: "unav"
excerpt: "It's a little powerful motor control board in 4x4cm and is open source and open hardware project is fully available on github. With this board you can control two DC brushed motors with different control law, position control, velocity control and torque control. The board works better with ROS."
classes: wide
number: 2014
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  teaser: /assets/project/unav/unav_small.png
  overlay_image: /assets/project/unav/unav-componenti.jpg
unav-history:
  - image_path: /assets/project/unav/RoboController.png
    alt: "Robocontroller"
    title: "Robocontroller"
    excerpt: "A commercial product designed by Mauro Soligo. This board had a dspic33 and different connectors to connect motors, h-bridges and other"
    url: "http://tuttoelettronica.net/archives/455"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /assets/project/motion-control/MotionControlParticolare.jpg
    alt: "Motion control"
    title: "Motion control"
    excerpt: "This is my board and was designed in 2008, a dsPIC33 Microchip controller and was a part of project during my bachelor degree."
    url: "/project/motion-control"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /assets/project/unav/dsNav33.png
    alt: "dsNav33"
    title: "dsNav33"
    excerpt: "developed by Guido Ottaviani, this board was designed before with three dsPIC30 and in the last release with one dsPIC33."
    url: "http://www.guiott.com/Rino/dsNavCon33/dsNavCon33.html"
    btn_label: "Read More"
    btn_class: "btn--primary"
unav-code:
  - title: "unav"
    excerpt: "The main repository with the motor controller, interaction system"
    url: "https://github.com/officinerobotiche/uNAV.X"
    btn_label: "Repository"
    btn_class: "btn--primary"
  - title: "or_bus_c.X"
    excerpt: "With this library the unav can communicate with a PC or another board with same protocol. In OR_BUS are collected all type of messages can send or receive."
    url: "https://github.com/officinerobotiche/or_bus_c.X"
    btn_label: "Repository"
    btn_class: "btn--primary"
  - title: "or_kernel_c.X"
    excerpt: "The heartbeats of the unav is written inside in this library. In this library are collected the system and task manager, the controller for the I2C, gpio, etc etc"
    url: "https://github.com/officinerobotiche/or_kernel_c.X"
    btn_label: "Repository"
    btn_class: "btn--primary"
  - title: "or_common_c.X"
    excerpt: "In this library are written the driver for eeprom, lcd, and other general math function."
    url: "https://github.com/officinerobotiche/or_common_c.X"
    btn_label: "Repository"
    btn_class: "btn--primary"
---

t's a little powerful motor control board in 4x4cm and is open source and open hardware project is fully available on github. With this board you can control two DC brushed motors with different control law, position control, velocity control and torque control. The board works better with ROS.

{% include figure image_path="/assets/project/unav/unav-history.png" alt="Unav history" caption="Unav history" %}

unav is a fusion from three different project. This project started during the autumn on 2014, and now more robot use this board.

{% include feature_row id="unav-history" type="left" %}

# How it's works

inside the unav beats an "home made" kernel that control all peripherals and with these can control two DC brushed motors. All code as written in MPLABX.

{% include figure image_path="/assets/project/unav/unavConnection.jpg" alt="Unav how it's work" caption="Unav how it's work" %}

{% include feature_row id="unav-code" type="center" %}