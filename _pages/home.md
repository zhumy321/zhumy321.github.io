---
layout: splash
# permalink: /  # 应该是这条，但是在本地得用/home/看才行
permalink: /home/   #注意这条可能要删掉 ???
hidden: true
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/mm-home-page-feature.jpg  # 这个图片要换掉哈???
  actions:
    - label: "<i class='fas fa-arrow-circle-right'></i> 最近发布"
      url: "/year-archive/" # 这个url可能也要改???
excerpt: >
  A flexible two-column Jekyll theme. Perfect for building personal sites, blogs, and portfolios.
feature_row:
  - image_path: /assets/images/about-intro.png # 要改???
    alt: "customizable" # 不知道alt是啥意思
    title: "框框1的名字"
    excerpt: "框框1的补充说明和摘要"
    url: "/about/" # 框框1下按钮跳转的网址, 是一个permalink
    btn_class: "btn--primary"
    btn_label: "去瞅一眼" # 框框1配套的跳转按钮
  - image_path: /assets/images/about-intro.png
    alt: "alt:"
    title: "框框2的名字"
    excerpt: "框框2的补充说明和摘要"
    url: "/about/"
    btn_class: "btn--primary"
    btn_label: "去瞅一眼"
  - image_path: /assets/images/about-intro.png
    alt: "alt:"
    title: "框框3的名字"
    excerpt: "框框3的补充说明和摘要"
    url: "/about/"
    btn_class: "btn--primary"
    btn_label: "去瞅一眼"      
---

{% include feature_row %}
