---
# examples go and see https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/
# gif的动图也是可以添加的哈

title:  用python操作Excel # 不写的话会从文件名自动生成。但标题不宜太长
excerpt: "" # 摘要，可不写
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
last_modified_at: 2024-08-01T19:00:02+08:00 # 可不写，但layout则要写。+8是东八区
categories: 
  - Jekyll
tags:
  - edge case
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

## Command line浅尝

其实我谷歌书签保留了很多网址可以放上来好查找的

可以参考的文档

中文的：[点击跳转](https://docs.xlwings.org/zh-cn/stable/converters.html)


英文的：[点击跳转](https://xlwings-jeroen.readthedocs.io/en/stable/api.html)

~~~
{

$ date
# 打印当前日期时间

$ echo Hello World!
# 打印出Hello World

# 展示当前目录print working directory
}
~~~

在Shell里面一般是这样：`username@hostname:current_directory`


![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2024-08-04_09-41-44.png)



| Wildcarts   | Represent |
| ----------- | ----------- |
| \*          | 用于匹配零个或多个任意字符      |
| \?          | 用于匹配任意单个字符           |
| \[\]        | 用于匹配方括号内的任意单个字符  |
| \[\!\]或\[\\] | 用于匹配除了方括号内的字符以外的任意单个字符  |
