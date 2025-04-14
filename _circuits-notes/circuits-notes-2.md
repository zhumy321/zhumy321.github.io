---
title:  Python碎片知识整理 # 
permalink: /circuits-notes/circuits-notes-chinese-2/
excerpt: "" # 摘要，可不写
# author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
author_profile: false # 让作者信息从sidebar消失
last_modified_at: 2025-04-13T22:54:00+08:00 # 
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

## 简单运算

python中3//2，这个符号是整除，结果是1 （余1）


## 解包

~~~

{
bomb = ['BANG', 'BOOM','BAM', 'POW','POOF',' 'PAH']
print(*bomb)
}
~~~

这里\*bomb是解包。即，如果直接print(bomb),，输出列表格式的bomb，也就是直接输出
`['BANG', 'BOOM','BAM', 'POW','POOF',' 'PAH']`
但是解包这样写的话，输出的会是`BANG BOOM BAM POW POOF PAH`
这个*的用法还可以用来捕获多余元素，如
~~~
first, *middle, last = [1, 2, 3, 4, 5]
print(first)   # 输出 1
print(middle)  # 输出 [2, 3, 4]
print(last)    # 输出 5
~~~




