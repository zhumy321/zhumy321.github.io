---
# examples go and see https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/
# gif的动图也是可以添加的哈

title:  一二三四 # 不写的话会从文件名自动生成。但标题不宜太长
excerpt: "" # 摘要，可不写
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写

# header: # 这张图会出现在文章页面的上方而且很大
#   image: /assets/images/img_20220803_221239.jpg
#   caption: Photo by the author # 图片水印，如"Photo credit: [**Unsplash**](https://unsplash.com)"

# header也可这么写：
# header:
  # teaser: "unsplash-gallery-image-2-th.jpg"

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

Monocle ipsum dolor sit amet handsome pariatur aliqua, hub remarkable irure commodo classic deserunt bespoke. Sunt commodo signature, Swiss minim flat white Tsutaya excepteur artisanal et Nordic laborum joy ANA. Beams mollit exquisite Ginza efficient dolore qui Comme des Garçons Winkreative Lufthansa bulletin global. Iconic sed liveable duis. Mollit dolore eu laboris Comme des Garçons hub pintxos sed eiusmod tote bag Shinkansen nisi consectetur pariatur. Nordic international quis finest Baggu dolore, bureaux hub hand-crafted ut joy sint Airbus A380.

Conversation handsome hub cosy, enim emerging sed K-pop velit Gaggenau charming proident et boulevard ryokan. Remarkable airport deserunt international est, nulla minim magna emerging discerning in exclusive dolor. Commodo dolore deserunt cosy, global Nordic culpa uniforms signature charming. Smart ryokan commodo, eiusmod global occaecat incididunt aliqua Beams. Boulevard conversation excepteur finest Swiss non veniam Comme des Garçons essential artisanal. Destination Scandinavian international, anim Boeing 787 in duis Baggu irure essential.

Fugiat exclusive laborum, Gaggenau ad Winkreative sharp elit labore. Remarkable officia ryokan Boeing 787, consectetur boutique Nordic Singapore espresso elit iconic perfect izakaya soft power excepteur. Ut veniam carefully curated K-pop dolore, uniforms in voluptate. Craftsmanship Ettinger Lufthansa sophisticated esse boutique veniam exquisite. Aute cillum bespoke, intricate consectetur in exquisite international lovely bulletin irure Washlet Gaggenau deserunt. Efficient eu quality of life wardrobe labore, dolor emerging airport concierge reprehenderit izakaya dolore liveable Baggu.

Commodo elegant essential consectetur Gaggenau culpa consequat id sophisticated St Moritz sunt conversation duis non velit. Nulla business class non ut Marylebone ANA soft power fugiat carefully curated. Bureaux sed punctual handsome Washlet impeccable hand-crafted aute extraordinary tote bag enim boulevard soft power sleepy. Dolore conversation irure Zürich the best adipisicing, vibrant finest hub anim premium aliqua. Cupidatat smart international, bureaux Baggu id efficient punctual. Tempor nulla flat white enim, K-pop incididunt elit efficient Toto uniforms concierge discerning. Concierge sleepy extraordinary, deserunt Melbourne commodo Nordic Winkreative Washlet Ginza exercitation espresso.

Tsutaya sed in business class sharp. Do Beams in adipisicing Lufthansa. Business class occaecat Melbourne, irure Singapore commodo espresso carefully curated quis quality of life adipisicing. Impeccable laborum efficient classic proident in. Beams Helsinki ullamco Marylebone dolore sophisticated concierge Muji anim duis joy ut. Comme des Garçons aute Muji in aliquip ryokan soft power Nordic essential ANA culpa elegant.

2024-07-21 20:50:38
相关笔记
#1 今天看了黄晓明参演的那部关于芯片的电视剧的片段，感觉很拉呀，要不我写个关于这个的小说去投稿吧？


Linux学习的内容：

俺的在线学习材料：

- [x] [LinuxJourney官网](https://linuxjourney.com/ "Click to go")
- [ ] [Linux Survival](https://linuxsurvival.com/ "Click to go")
- [ ] [Terminus](https://web.mit.edu/mprat/Public/web/Terminus/Web/main.html "Click to go")? Seem to be not available anymore. 
- [ ] [OverTheWire官网](https://overthewire.org/wargames/ "Click to go")
- [ ] [在线练习Linux系统](https://copy.sh/v86/?profile=linux26 "Click to go")
- [ ] [在vim-adventure学VIM](https://vim-adventures.com/ "Click to go")

## Command line浅尝

### Navigating

~~~
{

$ date
# 打印当前日期时间

$ whoami
# 比如你是root就会打印出来告诉你你是root

$ echo Hello World!
# 打印出Hello World

$ pwd
# 展示当前目录print working directory
}
~~~

在Shell里面一般是这样：`username@hostname:current_directory`

对应到我图中的实例则是:`root@VM-8-3-centos learn_linux`

其中root是用户名，VM-8-3-centos是hostname，learn_linux是当前目录

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Snipaste_2024-08-04_09-41-44.png)

~~~
{
$ cd .  

$ cd ..

$ cd ~

$ cd -
}
~~~

\. current directory 当前所在位置<br>
\.\. parent directory 去上一级目录<br>
\~ home directory 去最外面的目录<br>
\- previous directory) 回到刚刚的目录<br>
注意cd和.之间有个空格的哈


查看文件：
~~~
{
$ ls  
# 把当前文件夹的内容包括文件和文件夹展示出来

$ ls /home/lighthouse  
# 也可以指明展示哪一个文件夹的内容

$ ls -a   
# list all, 带.的隐藏文件也展示出来

$ ls -l   
# list long, 详细展示文件夹中各项内容的信息
# 从左至右: 
# file permissions, number of links, owner name, owner group, 
# file size, timestamp of last modification, and file/directory name.

$ ls -la   
# 结合了$ ls -a 和$ ls -l

$ ls -R
# 把当前文件夹的内容一个一个递归展示

$ ls -r
# ls出来的内容倒序查看

$ ls -t
# sort by modification time, newest first
}
~~~



`$ touch mynewfilename`
<br>Touch allows you to the create new empty files.


`$ file irenenewfile`
<br>查看这个file到底是个啥玩意. It will show you a description of the file’s contents.

综合以上，`$ touch irenenewfile`之后，就会有：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/learn_linux_ls_and_file.png)


###  Read a file
`$ cat filename`

cat指concatenate：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/learn_linux_cat.png)


`$ less`

直接进入文件里面查看内容，可以用翻页的方式看

Use the following command to navigate through less:

* q - 退出less回到shell
* Page up, Page down, Up and Down - 可以移动
* g - 去text文件的开头
* G - 去text文件的结尾
* /search - 在text文件里找内容，Prefacing the words you want to search with /
* h - help

### Repeat command

方向键上键就可以重复命令，如果是\!\!两个感叹号，则直接重复最后执行的那一个命令，查看所有历史命令则是用

`$ history`

所以如果你看完history又键入\!\!，就会是这样：

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/learn_linux_history.png)


`Ctrl + R`：输入Ctrl+R之后接着输之前输入过的命令，会弹出一些辅助选项，按Enter就可以了，有点像sublime text的tab键。

`tab` : 但tab在这里确实也可以自动补全

`clear` : 清除一下屏幕

### 复制

`$ cp filename1 /home/root/Documents/cooldocs`
把文件filename复制到路径/home/root/Documents/cooldocs中去

还有很好用的通配符。通配符的处理是由shell在执行命令之前进行的，而不是由具体的命令本身处理


| Wildcarts   | Represent |
| ----------- | ----------- |
| \*          | 用于匹配零个或多个任意字符      |
| \?          | 用于匹配任意单个字符           |
| \[\]        | 用于匹配方括号内的任意单个字符  |
| \[\!\]或\[\\] | 用于匹配除了方括号内的字符以外的任意单个字符  |


`$ ls *.txt` : 会列出当前目录下所有以.txt结尾的文件。

`$ cp \*.jpg /root/learn_linux/Pictures` : 会复制当前文件夹中所有的.jpg文件到文件夹Pictures中去

但是注意，cp默认只处理文件，而不处理目录，必须要加`-r`(这个-r表示copy over a directory?）来递归地复制目录，也就是说，如果你有以下文件和目录结构：
~~~
{
/home/user/documents/
    file1.txt
    file2.txt
    subdirectory/
        file3.txt
}
~~~
而你想将documents目录下的所有内容复制到backup目录中，但是backup目录目前并不存在。

如果你这样复制：
~~~
{
cp /home/user/documents/ /home/user/backup/
}
~~~
百分之百会失败

要这样才行，
~~~
{
cp -r /home/user/documents/ /home/user/backup/
}
~~~
这将复制documents目录下的所有内容，包括file1.txt，file2.txt，以及subdirectory/目录和其中的file3.txt，并创建backup目录。

所以最终的结果才会是你想要的这样：
~~~
{
/home/user/backup/
    file1.txt
    file2.txt
    subdirectory/
        file3.txt
}
~~~


复制时还有一个事情要考虑，就是假设你当前有一个名为report.txt的文件，你想将它复制到/backup目录中。如果/backup目录中已经存在一个名为report.txt的文件，你直接`
~~~
{
cp report.txt /backup/
}
~~~
就会无意中把原来/backup目录中的report.txt覆盖掉，这个时候最严谨的做法应该是
~~~
{
cp -i report.txt /backup/
}
~~~
这样系统会在覆盖之前询问你的决定。
