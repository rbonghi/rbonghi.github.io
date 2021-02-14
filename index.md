---
layout: splash
excerpt: "Robotics and computer vision"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/intro.jpg
  actions:
  - label: ":sparkling_heart: Sponsor"
    url: "https://github.com/sponsors/rbonghi"
  - label: "About me"
    url: "/about/"
intro: 
  - excerpt: 'Robotics and computer vision'
feature_row:
  - image_path: /assets/images/nanosaur.jpg
    alt: "NanoSaur"
    title: "🦕 NanoSaur"
    excerpt: "The smallest Jetson Nano Robot"
    url: "https://nanosaur.ai/"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /assets/images/panther.jpg
    alt: "Panther"
    title: "🐆 Panther"
    excerpt: "Panther an autonomous tracked robot"
    url: "https://rpanther.github.io/"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /assets/project/jetson-stats/jtop.gif
    alt: "jetson-stats"
    title: "📊 jetson-stats"
    excerpt: "Simple package to monitoring and control your NVIDIA Jetson [Xavier NX, Nano, AGX Xavier, TX1, TX2]"
    url: "/project/jetson-stats"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% include feature_row id="feature_row2" type="left" %}