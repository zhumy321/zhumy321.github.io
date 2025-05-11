---
title:  预留其他编程笔记专栏 # 
permalink: /circuits-notes/circuits-notes-chinese-3/
excerpt: "" # 摘要，可不写
# author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
author_profile: false # 让作者信息从sidebar消失
last_modified_at: 2024-08-03T15:42:00+08:00 # 
# redirect_from:
#   - /theme-setup/
toc: true # true, false都可以
toc_label: "目录" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true # "Stick" table of contents to the top of a page. true: toc floats. false: toc fixed
words_per_minute: 200 # 经我实验，中文则将WPM设置为30为好
# 英文则设为200
sidebar:
  title: "sidebar-circuits-notes"
  nav: sidebar-circuits-notes # 这是在yaml文件里你要找到的那个导航栏的名字
---

### Sublime Text 3积累用法

- 选中Sublime text中的所有文本，然后ctrl k，然后ctrl u，可以把所有文本变成大写。类似的，变小写则是ctrl + k，然后ctrl + L。




https://www.digikey.cn/zh/resources/conversion-calculators/conversion-calculator-wire-size

此工具用于计算线径的标称等效值，如美国线规 [AWG]、平方毫米面积 [mm²、圆密尔面积 [CMA] 等。只需输入已知测量值或导线号数，所有等效值即会自动计算并显示。

注意：本计算器的换算值基于实心导线。

美国线规 (AWG) 亦称“布朗-沙普”线规，于 1855 年制订。这种测量标准起源于计算导线通过模具拉拔的次数，以达到所需的尺寸。因此，线径大小跟号数是成反比的，并呈对数比例关系，也就是导线越粗，电线的 AWG 值越小，如 10 AWG 电线比 20AWG 电线的横截面积约要大上 10 倍。AWG 在北美和超过 65 个其他国家普遍使用。