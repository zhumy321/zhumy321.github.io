---
# examples go and see https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/
# gif的动图也是可以添加的哈

title:  学习Linux # 不写的话会从文件名自动生成。但标题不宜太长
# permalink: /docs/clock-in-diary-?/ 若是打工日记的文章，则要加这一个链接
excerpt: "" # 摘要，可不写
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写

# header: # 这张图会出现在文章页面的上方而且很大
#   image: /assets/images/img_20220803_221239.jpg
#   caption: Photo by the author # 图片水印，如"Photo credit: [**Unsplash**](https://unsplash.com)"

# header也可这么写：
# header:
  # teaser: "unsplash-gallery-image-2-th.jpg"

last_modified_at: 2024-08-03T15:42:00+08:00 # 可不写，但layout则要写。+8是东八区
categories: 
  - 正经的
tags:
  - 学习
toc: true # true, false都可以
toc_label: "目录" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true # "Stick" table of contents to the top of a page. true: toc floats. false: toc fixed
# link: https://github.com # 感觉不太对，这个link应该出现在超链接部分的引用中，但是试验后发现会变成文章标题的url，所以注释掉了

# yml文件values的默认设置如下，可以重新覆盖。图表上是可在https://fontawesome.com/start找
# layout: single
# author_profile: true # if false 则让作者信息从sidebar消失
# read_time: true
# comments: false
# share: true
# related: true
# show_date: true # true, false (default) 
# 以上都可以在post的此处覆盖

words_per_minute: 30 # 经我实验，中文则将WPM设置为30为好
# 英文则设为200

---

俺的在线学习材料：

- [x] [LinuxJourney官网](https://linuxjourney.com/ "Click to go")
- [ ] [Linux Survival](https://linuxsurvival.com/ "Click to go")
- [ ] [Terminus](https://web.mit.edu/mprat/Public/web/Terminus/Web/main.html "Click to go")? Seem to be not available anymore. 
- [ ] [OverTheWire官网](https://overthewire.org/wargames/ "Click to go")
- [ ] [在线练习Linux系统](https://copy.sh/v86/?profile=linux26 "Click to go")
- [ ] [在vim-adventure学VIM](https://vim-adventures.com/ "Click to go")

## Command line浅尝

`$ date`

`$ whoami`

`$ echo Hello World!`
<br>会打印出Hello World

### Navigating files

`$ pwd`
<br>会展示当前目录print working directory: 

~~~
{
$ cd .  

$ cd ..

$ cd ~

$ cd -
}
~~~
一个. current directory 当前所在位置<br>
两个. parent directory 去上一级目录<br>
一个~ home directory 去最外面的目录<br>
一个- previous directory) 回到刚刚的目录<br>
注意cd和.之间有个空格的哈


查看文件：
~~~
{
$ ls  
# list directories and files in the current directory by default

$ ls /home/lighthouse  
# You can specify which path you want to list the directories of

$ ls -a   
# list all, including the hidden files

$ ls -l   
# list long, shows a detailed list of files in a long format.
# starting from the left: 
# file permissions, number of links, owner name, owner group, 
# file size, timestamp of last modification, and file/directory name.

$ ls -la   
# 结合了$ ls -a 和$ ls -l

$ ls -R
# recursively list directory contents

$ ls -r
# reverse order while sorting

$ ls -t
# sort by modification time, newest first
}
~~~



`$ touch mynewfilename`
<br>Touch allows you to the create new empty files.


`$ file irenenewfile`
<br>查看这个file到底是个啥玩意. It will show you a description of the file’s contents.


###  Read a file
`$ cat dogfile birdfile`
<br> 指concatenate

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2024-08-03_20-24-42.png)


`$ less`
！！！


### Repeat command

`$ history`
！！！



加粗：前后各用2个星号包起来，加斜：前后各用1个星号包起来。删除线：两个~包裹起来



## 表格
使用三个或多个连字符（---）创建每列的标题，并使用管道（|）分隔每列。可以选择在表的任一端添加管道。

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```

