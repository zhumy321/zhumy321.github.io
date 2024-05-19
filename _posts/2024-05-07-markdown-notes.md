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
title:  Markdown notes整理自用 # 不写的话会从文件名自动生成。但标题不宜太长
excerpt: "测试文章用例：为方便自己查找而整理的markdown语法" # 摘要
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
# header: # 这张图会出现在文章页面的上方而且很大
#   image: /assets/images/img_20220803_221239.jpg
#   caption: Photo by the author # 图片水印，如"Photo credit: [**Unsplash**](https://unsplash.com)"
last_modified_at: 2024-05-07T19:12:02+08:00 # 可不写，但layout则要写。+8是东八区
categories: 
  - 正经的
tags:
  - 学习
toc: true # true, false都可以
toc_label: "目录" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true # "Stick" table of contents to the top of a page. true: toc floats. false: toc fixed
# link: https://github.com # 感觉不太对，这个link应该出现在超链接部分的引用中，但是试验后发现会变成文章标题的url，所以注释掉了
---



从这里开始是正文。其实如果愿意花时间看的话，在[Markdown语法官网](https://markdown.com.cn "最好的markdown教程")很清楚，但本文是精简整理给自己看的，同时作为github pages的一个测试文本。

以及提前说明，有一些比如换行、加粗这种操作有多种实现方式，有的编辑器支持，有的不支持，这里记录的都是兼容性比较高的，不容易出岔子

# 基本语法
## 标题
就是简单的# 标题的名字，井号的数量代表标题的级数。  下方也可以添加任意数量的 == 号来标识一级标题、 -- 号来标识二级标题。

## 换行
注意是换行，不是分段哈，换行指比如你现在看到123456789原本是在一起的，现在表现成：

我让这是第一行1234<br>56789这里从5开始是第二行，做到这一点则是在4和5中间插入<>，里面的内容写br。只需要写一次<>即可。

## 粗体
把要加粗的部分的前后各用2个星号包起来。

## 段落
空出一行就可以分段。注意，空出一行指有一行啥字也没有的内容卡在两段字中间，即上一段的句号+回车+回车+下一段的开头，这样才算是空了一行，上一段的句号后只回车一次就接下一段，是不会形成两段的。

对了，记得不要在开头空两个字的间隔，markdown文件的内容是靠着左边写的。

## 引用
在段落开头加一个>号即可。你也可以连续好几段开头都加>，引用内容为空白也可以，包含斜体啊或者列表什么的也可以。

嵌套引用也可以，比如“老师说鲁迅说过”，你可以第一段写>老师说，然后第二段写>>鲁迅说过。实现起来就会是这个样子：
> 老师说
>> 鲁迅说过


## 插入代码
把代码部分前后用反引号`包起来就可以。

比如反引号int main反引号，实现表现就会是这个样子：
`int main`

如果代码内容里有反引号，那你就把外面那个包裹整个代码部分的反引号改成双反引号就行。

## 分割线
空出三行，都不写任何内容，只在中间那行单独写三个星号、三个下划线或者三个破折号都可以，他们实际表现看起来都一样，就像这样：

---

## 插入链接
这么写： 中括号超链接显示出来的名字中括号(对应的网址 "鼠标悬浮在网址上时出现的名字")

放在中括号里的是网页上看到的字，链接的网址放在后面的括号中，后面这个链接title可选写或不写。

比如如果你写 中括号名字是Markdown语法官网中括号(https://markdown.com.cn "这里是鼠标悬浮是出现的链接文本")

那么实际表现出来就会是：
[名字是Markdown语法官网](https://markdown.com.cn "这里是鼠标悬浮是出现的链接文本")

---

如果你只是放一个链接，不给它起名字，它看起来就是一个链接的样子，那可以把它用<>包起来，看起来就会是这样<https://markdown.com.cn>

## 类参考文献的引用
这是一种特殊的链接，由两部分组成，引用的时候写一个部分，另一个部分你可以认为是汇总，汇总的这部分可以放在文档的任意处。

第一部分就是两对中括号，第一对里写你给链接起的名字，第二对里写标签如1或a等，标签不区分大小写，写字母，数字，空格或标点符号都可以。

如：[给链接起的名字][1]

第二部分写：一对中括号，冒号，然后是链接。中括号里的是序号，如
中括号序号中括号:http://巴拉巴拉


## 列表
有序：数字+英文句点即可。 数字不必按数学顺序排列，但是列表应当以数字 1 起始。
无序：在列表项前面添加破折号、星号、加号均可，挑一种用就行。缩进一个或多个列表项可创建嵌套列表。

## 图片
`![图片的替代文本](图片的存放地址或者链接 "给图片加标题但不加也行")(这还有个可选的地方填图片的网络链接，就是点击图片可以跳转的那种)`

## 转义
在要转义的字符前面加enter键旁边的那个斜杠就可以。
## 内嵌HTML

# 拓展语法
## 删除线
用两个`~把要删除的部分前后包裹起来就可以（跟用两个星号加粗字体是一样的用法）

## 任务列表语法
- [x] 做好删改
- [ ] 上传github
- [ ] 检查网站现状

## 表格
使用三个或多个连字符（---）创建每列的标题，并使用管道（|）分隔每列。可以选择在表的任一端添加管道。

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```

出来就会是这样：
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

表格对齐等

## 围栏代码块
在代码块之前和之后的行上使用三个反引号（(```）或三个波浪号（~~~）
~~~
\~~~
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
\~~~
~~~

出来就会是这样：

~~~
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
~~~

## 脚注


## 标题编号


## 定义列表


## emoji
有两种方法可以加入emoji表情，第一种是你直接去复制黏贴这个表情（如果你的应用程序支持，那在你黏贴之后表情会自动变成对应的HTML之类的表示，不过注意HTML页面编码得要是UTF-8）。emoji表情可以在这里找到
[emojipedia](https://emojipedia.org/)

另一种则是键盘敲emoji shortcodes，他们是表情符号的名字，以英文冒号开头和结尾。比如帐篷的emoji，你可以在markdown里面手敲为   冒号tent冒号，出来就会是这样:tent:

笑哭则是 冒号joy冒号，出来就会是这样 :joy:


## 自动网址链接