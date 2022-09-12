---
layout: splash
title: "rnext"
excerpt: "I'm Raffaello Bonghi an Italian enthusiastic robotics engineer, born in the eternal city of 🛵 Rome."
tagline: "Robotics & Automation<br/> <small>Welcome to <b>Raffaello Bonghi</b> website!</small>"
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/posts/MFR/2018/01-MFR2018.jpg
  actions:
  - label: ":sparkling_heart: Sponsor"
    url: "https://github.com/sponsors/rbonghi"
  - label: "About me"
    url: "/raffaello-bonghi"
  - label: "Contact"
    url: "/contact"
intro: 
  - excerpt: "<big>Hello! Welcome here!</big><br/> I'm **Raffaello Bonghi** an 🇮🇹 **Italian** enthusiastic 🤖 **robotics** engineer, born in the eternal city of 🛵 **Rome** and now I'm living in 🇬🇧 England.<br/><br/> I [studied](/raffaello-bonghi) systems automation and robotics at  👨‍🎓  **University of Rome La Sapienza** and 👨‍🎓  **Universite Paris-Sud**, but I always made [**robots**](/robot/) and open-source [**projects**](/project/)!"
feature_row:
  - image_path: https://nanosaur.ai/assets/images/intro.jpg
    alt: "nanosaur"
    title: "🦕 nanosaur"
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
footer: 
  - excerpt: 'I am proudly part of :pizza: [pizzarobotics](https://pizzarobotics.org) community'
---

{% include feature_row id="intro" type="center" %}

{% include feature_row %}

{% include feature_row id="footer" type="center" %}

{% include latest_posts %}
