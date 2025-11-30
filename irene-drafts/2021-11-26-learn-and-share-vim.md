---
# examples go and see https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/
# gif的动图也是可以添加的哈

title:  vim学习与分享 # 不写的话会从文件名自动生成。但标题不宜太长
excerpt: "" # 摘要，可不写
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
last_modified_at: 2024-08-01T19:00:02+08:00 # 可不写，但layout则要写。+8是东八区
categories: 
  - 正经的
tags:
  - 学习
toc: false
toc_label: "目录" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true
words_per_minute: 30 # 经我实验，中文则将WPM设置为30为好
# 英文则设为200

---

vim这个玩意的最初印象，来自于在网络上的一些笑话——打开vim界面后一脸懵逼，只好重启来退出云云([从vi - How do I exit the Vim editor? - Stack Overflow来看确实不假](https://stackoverflow.com/questions/11828270/how-do-i-exit-the-vim-editor)）。于是知难而退。可接触服务器以后就明白了，vim这个编辑器是不会也得会的。探索后发现，它也不是那么难，甚至觉得很方便。了解一段时间后觉得，Swaroop的A Byte  of Vim写得很好。上网一查它有一个中文版（ [A Byte of Vim (Chinese) — A Byte of Vim (Chinese) documentation (a-byte-of-vim-chinese.readthedocs.io)](https://a-byte-of-vim-chinese.readthedocs.io/en/latest/index.html) ），但可惜的是不知道咋的，这位朋友没有翻译完。所以我想开一个vim的专栏，记录和分享一下vim的学习。

因为我主要是跟这本书学的，所以这次写主要是翻译一下Swaroop 先生的A Byte of Vim, v0.51 (for Vim version 7)，原书可以在[Swaroop 先生自己的网站](https://swaroopch.com/)上找到。
另外还有一个小姐姐做的[网站](https://vimjc.com/)我也觉得挺好的，只是不知何故，2020年3月后就没有更新了。

立个flag，如果我真能把这本书翻译完，我就去给Swaroop大佬发邮件，告诉他现在真的真的有中文版了！
