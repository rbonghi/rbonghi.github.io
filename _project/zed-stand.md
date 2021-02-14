---
title: "ZED stand"
excerpt: "A little stand to block your ZED camera in your robot, drone. To build this stand is required a 3D printer, a photographic screw, and if you want a spray."
classes: wide
number: 2016
link: https://grabcad.com/library/zed-stand-1
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/project/zed-stand/zed-stand_3.jpeg
  teaser: /assets/project/zed-stand/zed-stand_3.jpeg
  actions:
    - label: "Grabcad"
      url: "https://grabcad.com/library/zed-stand-1"
    - label: "Thingverse"
      url: "https://www.thingiverse.com/thing:3208903"
zed-stand:
  - url: /assets/project/zed-stand/zed-stand_7.jpg
    image_path: /assets/project/zed-stand/zed-stand_7.jpg
    alt: "ZED stand rendering front"
    title: "ZED stand rendering front"
  - url: /assets/project/zed-stand/zed-stand_6.jpg
    image_path: /assets/project/zed-stand/zed-stand_6.jpg
    alt: "ZED stand rendering components top"
    title: "ZED stand rendering components top"
  - url: /assets/project/zed-stand/zed-stand_5.jpg
    image_path: /assets/project/zed-stand/zed-stand_5.jpg
    alt: "ZED stand rendering components down"
    title: "ZED stand rendering components down"
zed-specifications:
  - url: /assets/project/zed-stand/zed-stand_layout.jpg
    image_path: /assets/project/zed-stand/zed-stand_layout.jpg
    alt: "ZED layout"
    title: "ZED layout"
  - url: /assets/project/zed-stand/zed-stand_layout_2.jpg
    image_path: /assets/project/zed-stand/zed-stand_layout_2.jpg
    alt: "ZED layout"
    title: "ZED layout"
zed-stand-print:
  - url: /assets/project/zed-stand/zed-stand_printer_1.jpg
    image_path: /assets/project/zed-stand/zed-stand_printer_1.jpg
    alt: "ZED stand print status"
    title: "ZED stand print status"
  - url: /assets/project/zed-stand/zed-stand_printer_2.jpg
    image_path: /assets/project/zed-stand/zed-stand_printer_2.jpg
    alt: "ZED stand print setup"
    title: "ZED stand print setup"
  - url: /assets/project/zed-stand/zed-stand_4.jpeg
    image_path: /assets/project/zed-stand/zed-stand_4.jpeg
    alt: "ZED stand print parts"
    title: "ZED stand print parts"
  - url: /assets/project/zed-stand/zed-stand_3.jpeg
    image_path: /assets/project/zed-stand/zed-stand_3.jpeg
    alt: "ZED stand overview"
    title: "ZED stand overview"
  - url: /assets/project/zed-stand/zed-stand_1.jpeg
    image_path: /assets/project/zed-stand/zed-stand_1.jpeg
    alt: "ZED stand build"
    title: "ZED stand build"
  - url: /assets/project/zed-stand/zed-stand_2.jpeg
    image_path: /assets/project/zed-stand/zed-stand_2.jpeg
    alt: "ZED stand overview"
    title: "ZED stand overview"
parts:
  - url: /assets/project/zed-stand/zed-stand_screw.jpeg
    image_path: /assets/project/zed-stand/zed-stand_screw.jpeg
    alt: "ZED stand screw"
    title: "ZED stand screw"
  - url: /assets/project/zed-stand/zed-stand_screw_dimension.jpg
    image_path: /assets/project/zed-stand/zed-stand_screw_dimension.jpg
    alt: "ZED stand screw"
    title: "ZED stand screw"
---

The ZED Stereo Camera made from [stereolabs](https://www.stereolabs.com/) is a lightweight depth sensor based on passive stereovision.

The technology of the ZED stereocamera is an integrate controller to generate from the two cameras the disparity map and all camera correction source after camera calibration.

This sensor have a particular feature optimal for robotics application:
* Outputs a high resolution video on USB 3.0 with synchronized video streams
* Max video mode with 2.2k at 15k frames per second, output 4416x1242 px
* Depth range: 1.5 - 20m
* Camera baseline: 120mm
* Dimension: 175 x 30 x 33 mm
* Weight: 159 g

{% include figure image_path="/assets/project/zed-stand/zed-camera.jpg" alt="ZED architecture" caption="ZED architecture" %}

When you buy a ZED in the box you have the sensor, a usb pen drive with all driver, a documentation and a mini stand tripod.

{% include gallery id="zed-stand" caption="ZED parts" %}

This tripod isn't useful when you use for robotics application and you want fix strongly in your chassis.  To solve this problem I've build a new stand to align the sensor with plane, because this camera have a **format of 3,8°** from rear side to camera side.

{% include gallery id="zed-specifications" caption="ZED specifications" %}

The ZED stand have maximum size of **35 x 50 x 14 mm**. It's divided in two parts. The first one is to screw the stan to the chassis, the second one to connect with a photographic screw to zed camera.

All information about weight are collected in the following list:
* **Upper** 8 gram
* **Lower** 9 gram
* **Total with all screws** 24 gram
* **With ZED sensor assembled** 183 gram

In the following gallery, the all step to print this stand and a test

{% include gallery id="zed-stand-print" caption="ZED parts print" %}

This Stand is available on grabcad, you can find a 3D model and a technical drawings with all detailed information about this ZED stand. You can buy a photographic screw from [amazon](https://www.amazon.it/gp/product/B00IXD10BO)

{% include gallery id="parts" caption="screw" %}

