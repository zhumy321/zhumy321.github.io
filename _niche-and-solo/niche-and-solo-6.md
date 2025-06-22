---
title:  Minimal Mistakes的Win10本地预览 # 不写的话会从文件名自动生成。但标题不宜太长
permalink: /niche-and-solo/6/
excerpt: "Minimal Mistakes" # 摘要，可不写
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
author_profile: false # 让作者信息从sidebar消失
last_modified_at: 2025-05-08T15:43:00+08:00 # 可不写，但layout则要写。+8是东八区
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

## 本地环境查看

ruby、bundle、jekyll是三个必要条件

> 这种情况就是现在三个必要条件都缺少：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250430182307.png)


## 1. 安装Ruby和Bundler（仅需一次）

去官网[RubyInstaller.org](https://rubyinstaller.org/downloads/ "点击跳转") 下载Ruby+Devkit，并运行下载好的.exe文件：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250509115259.png)

> a. 在安全警告中点击运行：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250429154825.png)

> b. 选择为自己安装还是为所有用户安装：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250429154902.png)

> c. 同意License：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250429155026.png)

> d. 选择安装路径，记得勾上add to PATH：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250429155045.png)

> e. 选组件，一般就默认就行：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250429155559.png)

> f. 等待安装完毕：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250429155620.png)

> g. 点击Finish完成：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250429160017.png)

> h. 出现该界面就是成功安装完毕了：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250429160045.png)

> i. 所以现在有Ruby、Bundle，缺个Jekyll 

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250430183313.png)


>！如果在i步骤中没有Bundler，则去命令行（要有管理员权限哈）

`gem`是 Ruby 的包管理工具，安装后会全局可用。
输入`gem install bundler`
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250430113631.png)


## 2. 装Jekyll（仅需一次）

> a. cd到项目所在的文件夹，然后输入bundle

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250430183857.png)

> b. 然后等fetching完和install完，

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250430183944.png)

> c. 此时运行Jekyll serve就可以了。有一种情况是原来的默认端口被占用了：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250430184058.png)

> d. 此时则不要用命令Jekyll serve，改用bundle exec且换一个端口：`bundle exec jekyll serve --port 4001`

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250430184339.png)

## 3. 本地预览（每次）

> 后续在确定依赖项都安装好的情况下：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250430181927.png)

需要预览时，cd到项目文件夹，并`jekyll serve`或`bundle exec jekyll serve --port 4001`即可

!

## 如何卸载Ruby和Bundler

1. 控制面板->卸载程序->![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250430095729.png)
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Pasted image 20250430095812.png)

2. 删除用户目录下的 Ruby 相关文件夹
- 删除 Ruby 安装目录（默认路径如 `C:\Ruby33-x64`）。
- 删除用户目录下的 Ruby 相关文件夹：
    ```
    C:\Users\你的用户名\.gem
    C:\Users\你的用户名\.bundler
    ```

## 参考资料

[^1]:[github docs] https://docs.github.com/zh/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll


[^2]:[jekyllrb] https://jekyllrb.com/docs/installation/windows/

[^3]:[Remote theme method] https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/#remote-theme-method "Permalink")



