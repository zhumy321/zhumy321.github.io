---
layout: splash
permalink: / 
hidden: true
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/seaside-fireworks-with-friends.png
  caption: Photo by the best friends ever in SZU Bandclub 
  actions:
    - label: "<i class='fas fa-arrow-circle-right'></i> 最近发布"
      url: "/year-archive/" # 这个url可能也要改???
# excerpt: >
#   A flexible two-column Jekyll theme. Perfect for building personal sites, blogs, and portfolios. # 这是飘在overlay图片上的文字
feature_row:
  - image_path: /assets/images/riding-bike.jpg
    alt: "customizable" # 不知道alt是啥意思
    title: "生活"
    excerpt: "Life and serendipities."
    url: "/tags/#生活" # 框框1下按钮跳转的网址, 是一个permalink
    btn_class: "btn--primary"
    btn_label: "去瞅一眼" # 框框1配套的跳转按钮
  - image_path: /assets/images/captive-of-theskyscraper.jpg
    alt: "alt:"
    title: "想法"
    excerpt: "The world and the meanings."
    url: "/tags/#想法-杂谈"
    btn_class: "btn--primary"
    btn_label: "去瞅一眼"
  - image_path: /assets/images/img_20211117_134334.jpg
    alt: "alt:"
    title: "学习"
    excerpt: "Am I better than yesterday?"
    url: "/tags/#学习"
    btn_class: "btn--primary"
    btn_label: "去瞅一眼"      
---

{% include feature_row %}
