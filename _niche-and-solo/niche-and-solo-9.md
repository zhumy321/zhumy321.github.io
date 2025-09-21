---
title: 用Python的manim做动画 # 不写的话会从文件名自动生成。但标题不宜太长
permalink: /niche-and-solo/9/
excerpt: "" # 摘要，可不写
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
author_profile: false # 让作者信息从sidebar消失
last_modified_at: 2025-09-13T11:59:00+08:00 # 可不写，但layout则要写。+8是东八区
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


## 前置条件

### 安装Python和Sublime Text编辑器

已经写过，此处不再赘述。[Sublime Text 3配置Python和C环境（Win 10）](https://zhumy321.github.io/%E6%AD%A3%E7%BB%8F%E7%9A%84/sublime-text-3-C-and-python/)

### 安装FFmpeg

去到[FFmpeg.org](https://ffmpeg.org/)

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-01-47.png)

选择你自己用的系统对应的版本，如我的windows用这个:Windows biulds byBtbN

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-02-34.png)

点进去会跳转到Github仓库，把这里的assets展开

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-11-45.png)

然后下载最新的：ffmpeg-master-latest-win64-gpl-shared.zip

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-13-31.png)


下载完毕后，要验证文件完整性（防下载出错/篡改）:

- 管理员身份打开 PowerShell

- 在PowerShell用以下命令查看哈希值，注意FFmpeg压缩包的路径要正确：`Get-FileHash -Path "C:\Users\irene-z\Downloads\ffmpeg-master-latest-win64-gpl-shared.zip" -Algorithm SHA256`:![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-21-01.png)

- 如哈希值一致，说明压缩包完好![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-23-43.png)

- 那么就可以解压、放到你指定的那个文件夹里了 ![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-26-43.png) ![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-32-27.png)


最后添加到环境变量：右键点击“此电脑” →“ 属性” →“ 高级系统设置” →“ 环境变量”，在系统变量中找到“Path”，点击“新建”，然后输入解压后 bin/ 的路径，最后点击“确定”即可。
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-36-23.png)


至此，如在命令行中输入：`ffmpeg -version`，应有版本输出，说明安装成功

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-41-01.png)


### 安装Manim库

在命令行输入`pip install manim`即可

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-46-20.png)

### 安装LaTeX（选装）


### 新增Sublime Text的编译系统

此时，直接在Sublime Text里运行python代码，只是运行了Python解释器，无法直接运行 Manim 代码并生成视频，因为 Manim 需要特定的命令行指令来触发渲染。

如：`manim test.py SceneName -pqm`

所以此时比较方便的方式是直接在sublime text中构建一个新的编译系统，给manim用：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-55-30.png)


```
{
    "cmd": ["manim", "$file", "${file_base_name}", "-pqm"],
    "selector": "source.python",
    "working_dir": "$file_path"
}
```


![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_22-58-37.png)



在运行程序时，将编译系统选为manim即可。

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2025-09-20_23-07-00.png)


## 开始做动画


