---
title: 编曲软件操作笔记 # 不写的话会从文件名自动生成。但标题不宜太长
permalink: /niche-and-solo/10/
excerpt: "" # 摘要，可不写
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
author_profile: false # 让作者信息从sidebar消失
last_modified_at: 2025-08-02T09:59:00+08:00 # 可不写，但layout则要写。+8是东八区
categories: 
  - 正经的
tags:
  - 学习
toc: true # true, false都可以
toc_label: "TOC" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true # "Stick" table of contents to the top of a page. true: toc floats. false: toc fixed
words_per_minute: 30 # 经我实验，中文则将WPM设置为30为好
# 英文则设为200
sidebar:
  title: "自娱自乐"
  nav: sidebar-niche-and-solo # 这是在yaml文件里你要找到的那个导航栏的名字
---

## 打开工程时

- 设置工程参数：采样率（Sample Rate，大多是48kHz）和比特率(Record Format，通常是24或者32bit)


- 设置当前音乐作品的参数：速度和节拍，在走带控制器中设置(如3/4, 120bpm)。


## 建立轨道

有很多track类型，用的最多的是音频audio，乐器instrument，MIDI轨道（编曲过程中都是MIDI轨）

常用的Mono是单声道（录音用的多），sterio是立体声（导入时用的多），大部分时候用立体声

建立轨道后可以直接把音频文件拖拽进来，会弹出对话框，确认是否将导入的源音频文件复制一份放到工程目录内，一般建议勾选。其他都一般是默认的。


新建MIDI轨道后，新建MIDI片段，然后从MIDI输出通道的设置里加载指定的音源，双击这个轨道的内容就会来到MIDI编写的钢琴卷帘窗，就可以输入各种音符。












