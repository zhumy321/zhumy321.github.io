---
# 注意哈??? 研究网站的时候记得去https://mmistakes.github.io/minimal-mistakes/docs/configuration/逐一检查配置。至于图表，在https://fontawesome.com/start找



# yml文件中对posts的values的默认设置：
# layout: single
# author_profile: true # if false 则让作者信息从sidebar消失
# read_time: true
# comments: false
# share: true
# related: true
# show_date: true # true, false (default) 感觉这两行没有用啊
# 以上都可以在post的此处覆盖  
# 你需要在post中单独新增的：
title:  "测试文本文章2" # 不写的话会从文件名自动生成。但标题不宜太长
excerpt: "这是文章2的摘要。" # 摘要
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
header: # 这张图会出现在文章页面的上方而且很大
  image: /assets/images/img_20220803_221239.jpg
  caption: Photo by the author # 图片水印，如"Photo credit: [**Unsplash**](https://unsplash.com)"
last_modified_at: 2024-04-27T13:30:02+08:00 # 可不写，但layout则要写。+8是东八区
categories: 
  - 回忆录
tags:
  - 本站
  - 生活
  - 杂谈
  - 学习
toc: true # true, false都可以
toc_label: "目录名字随便取" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: false # "Stick" table of contents to the top of a page
# link: https://github.com # 感觉不太对，这个link应该出现在超链接部分的引用中，但是试验后发现会变成文章标题的url，所以注释掉了
---


下方是正文。其实正文不写也可以。

## 测试内容一览

今天要做的事情不多
* 整个网站架构弄清楚
* 练琴

### 排序
1. 第一项
2. 第二项
  * 无序项a
  * 无序项b
  1. 有序项a
  2. 有序项b
  * 无序项c
3. 第三项
4. 第四项


### 动作清单

- [x] 做好删改
- [ ] 上传github
- [ ] 检查网站现状

### 引用一句名言

> Only one thing is impossible for God: To find any sense in any copyright law on the planet.
  
> <cite><a href="http://www.brainyquote.com/quotes/quotes/m/marktwain163473.html">Mark Twain</a></cite>


### 超链接
因为这个theme supports **link posts**, made famous by John Gruber. To use, just add `link: http://url-you-want-linked` to the post's YAML front matter and you're done：

> And this is how a quote looks.

也可以在最顶上定义link（已经定义好了），然后正文中引用也可：Some [link](#) can also be shown.



### inline代码示例
This is the post content with inline code, (e.g. `<span style="color: red;">red</span>`. It should be displayed in place of the auto-generated excerpt in single-page views. Archive-index pages should display an auto-generated excerpt of this content.

Be sure to test the formatting of the auto-generated excerpt, to ensure that it doesn't create any layout problems.



## 一段对话
Abbott: Strange as it may seem, they give ball players nowadays very peculiar names.

Costello: Funny names?

Abbott: Nicknames, nicknames. Now, on the St. Louis team we have Who's on first, What's on second, I Don't Know is on third--

Costello: That's what I want to find out. I want you to tell me the names of the fellows on the St. Louis team.

Abbott: I'm telling you. Who's on first, What's on second, I Don't Know is on third--

Costello: You know the fellows' names?

Abbott: Yes.

Costello: Well, then who's playing first?

Abbott: Yes.

Costello: I mean the fellow's name on first base.

Abbott: Who.

Costello: The fellow playin' first base.

Abbott: Who.

Costello: The guy on first base.

Abbott: Who is on first.

Costello: Well, what are you askin' me for?

Abbott: I'm not asking you--I'm telling you. Who is on first.

Costello: I'm asking you--who's on first?

Abbott: That's the man's name.

Costello: That's who's name?

Abbott: Yes.

Costello: When you pay off the first baseman every month, who gets the money?

Abbott: Every dollar of it. And why not, the man's entitled to it.

Costello: Who is?

Abbott: Yes.

Costello: So who gets it?

Abbott: Why shouldn't he? Sometimes his wife comes down and collects it.

Costello: Who's wife?

Abbott: Yes. After all, the man earns it.

Costello: Who does?

Abbott: Absolutely.

Costello: Well, all I'm trying to find out is what's the guy's name on first base?

Abbott: Oh, no, no. What is on second base.

Costello: I'm not asking you who's on second.

Abbott: Who's on first!

Costello: St. Louis has a good outfield?

Abbott: Oh, absolutely.

Costello: The left fielder's name?

Abbott: Why.

Costello: I don't know, I just thought I'd ask.

Abbott: Well, I just thought I'd tell you.

Costello: Then tell me who's playing left field?

Abbott: Who's playing first.

Costello: Stay out of the infield! The left fielder's name?

Abbott: Why.

Costello: Because.

Abbott: Oh, he's center field.

Costello: Wait a minute. You got a pitcher on this team?

Abbott: Wouldn't this be a fine team without a pitcher?

Costello: Tell me the pitcher's name.

Abbott: Tomorrow.

Costello: Now, when the guy at bat bunts the ball--me being a good catcher--I want to throw the guy out at first base, so I pick up the ball and throw it to who?

Abbott: Now, that's he first thing you've said right.

Costello: I DON'T EVEN KNOW WHAT I'M TALKING ABOUT!

Abbott: Don't get excited. Take it easy.

Costello: I throw the ball to first base, whoever it is grabs the ball, so the guy runs to second. Who picks up the ball and throws it to what. What throws it to I don't know. I don't know throws it back to tomorrow--a triple play.

Abbott: Yeah, it could be.

Costello: Another guy gets up and it's a long ball to center.

Abbott: Because.

Costello: Why? I don't know. And I don't care.

Abbott: What was that?

Costello: I said, I DON'T CARE!

Abbott: Oh, that's our shortstop!
