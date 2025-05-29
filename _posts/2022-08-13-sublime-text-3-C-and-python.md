---
title:  Sublime Text 3配置Python和C环境（Win 10） # 不写的话会从文件名自动生成。但标题不宜太长
excerpt: "" # 摘要，可不写
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
last_modified_at: 2022-08-13T19:00:02+08:00 # 可不写，但layout则要写。+8是东八区
categories: 
  - 正经的
tags:
  - 学习
toc: true # true, false都可以
toc_label: "目录" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true # "Stick" table of contents to the top of a page. true: toc floats. false: toc fixed
words_per_minute: 30 # 经我实验，中文则将WPM设置为30为好
# 英文则设为200

---


## Sublime Text 3

### 安装Sublime Text 3

- 先去官网[Sublime Text 3官网](https://www.sublimetext.com/3)下载Sublime Text 3，选择自己需要的版本即可，
流程如下：
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-1.png)

- 把下载下来的.exe文件用管理员身份运行：
![图-2](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-2.png)

- 选择安装的路径，然后点Next：
![图-3](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-3.png)

- 建议勾选加入菜单，然后点Next：
![图-4](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-4.png)

- 点击install开始安装：
![图-5](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-5.png)

- 安装完毕之后点Finish：
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-6.png)

- 然后点击菜单，Sublime Text 3出现在开始菜单里，就安装好啦
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-7.png)

- 打开后如下图：（这里新版本提示界面点取消就好了，因为Sublime Text现在已经出到了4，但是3也还是很好用的）
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-8.png)



### 安装Package Control插件

- 打开Tools菜单下的Command Paletter，或者使用ctrl+shift+p快捷键，来打开Sublime Text 3的命令面板。在命令面板中输入install找到安装Package Control插件的选项，鼠标左键或者回车安装Package Control
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-9.png)


- 安装好后会有提示
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-10.png)

- 重新进入Command Paletter，输入Package Control可以在下拉列表里找到“Install package”选项（如果没有，则在安装先后重启Sublime Text 3，再进入Package Control 即可），这样就可以安装插件了
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-11.png)



### 用Package Control安装常用插件

下面以中文汉化插件为例。<br>

- ctrl+shift+p把命令面板叫出来，在命令面板输入（或找到）Package Control：Install package，鼠标左键点击或方向键选中并回车进入。
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-11.png)

- 此时左下方会有一个小等号来回移动提示你等待一会，联网后完成后会出现插件列表
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-12.png)

- 插件列表大概如下：
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-13.png)


- 输入插件的全名或部分名字，比如输入chinese，然后可以在下拉的联想菜单里选中ChineseLocalizationgs插件，左键单击（或移动方向键选中并回车）即可安装
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-14.png)

- 左下角再次出现小等号，等待一会。插件安装好后会在新页面弹出提示，同时可以看到整个界面已经变成中文了（如果没有，尝试重启Sublime Text 3 ）：
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-15.png)

- 这个时候就可以进入帮助[Help]菜单，语言[Language]选项后就可以选择中文或者切换回英文。
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-16.png)


- 注意，已经安装过的插件，你再回到Package Control页去搜就搜不到了

### 一些插件说明（个人向）

大部分插件都可以在菜单栏中找到或者配置
#### colorsublime，可以安装不同的主题（在命令面板，或者preferences处可以选择主题）。我个人喜欢暗色的界面、同时对常用编程语言高亮比较顺眼的主题.
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-17.png)
 
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-18.png)


#### 最近比较喜欢chameleon。（图中用的是python举例）
![图-1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_download-19.png)

#### [sublimerge](https://www.sublimerge.com/)可以比较不同文件的内容。

#### ConvertToUTF8，可以解决中文乱码问题

#### Markdown Preview
To be added…



## 配置C环境


### 下载MinGW



- 前往官网下载自己所需要的MinGW版本即可，流程如下：
- 如果有网，下载了.exe文件后直接点击执行即可(https://sourceforge.net/projects/mingw/)。此处举例主要是离线安装哈：下载好安装MinGW压缩包( https://sourceforge.net/projects/mingw-w64/ 选择files然后往下拉)，zip或者7z都可以 
- 在你想指定的文件夹下新建MinGW文件夹（可以是Program Files (x86)也可以直接在C盘，或者你希望放的其他文件夹），把解压之后的mingw64文件夹放到MinGW下

![图1-4](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_C_Edited_1_4.png)

- 注意，解压好的文件夹内会有一个bin文件夹。去系统   环境变量   添加MinGW64 bin路径。你可以右键单击“此电脑”，选择“属性”->“高级系统设置”->“高级”->“环境变量”进入设置环境变量的页面，也可以直接在搜索栏搜索“环境变量”
- 选中系统变量的“Path”，点击“编辑”，然后选择“新建”，添加好路径后点击“确定”
![图5-8](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_C_Edited_6_10.png)

- 测试一下 gcc/g++，看装好了没。 打开命令行（可以通过win + R，输入“cmd”唤出命令行，或者在桌面win + X唤出windows power shell），分别输入 gcc -v 和 g++ -v ，如图有正常响应即可

![图9-11](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_C_Edited_11_12.png)




### 在Sublime里面编译C

- 在Sublime Text 3里build一个new的system（新建编译系统），配置如下，可以保存命名为C（你自己认得就行）

```
{    
    "cmd"        : ["gcc","${file}", "-o", "${file_path}/${file_base_name}"],
    "file_regex" :"^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
    "working_dir":"${file_path}",
    "selector"   : "source.c",
    "encoding"   : "utf8",
    
    "variants"   :
    [
        {
            "name"  : "Run",
            "cmd"   : ["cmd","/c", "gcc", "${file}", "-o", "${file_path}/${file_base_name}","&&", "cmd", "/c","${file_path}/${file_base_name}"]
        },
        {
            "name"  :"RunInCommand",
            "cmd" : ["cmd","/c", "gcc", "${file}", "-o","${file_path}/${file_base_name}", "&&","start","cmd","/","${file_path}/${file_base_name} && pause"]
        }
    ]
}
```
![图12-13](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_C_Edited_13_14.png)


- 再打开Tools -> Build System，可以看到出现了刚才保存好的C的编译系统

- 在Sublime Text 3里新建一个文件，输入一小段C代码做测试，如图。选择右下角的Plain Text，会弹出上拉列表，可以在列表中选择当前代码是C语言，这样Sublime Text 3会以C的语法高亮对应代码。保存这个文件为test.c

- 在Sublime Text 3中按快捷键Ctrl + B，选Run即可


![图14-16](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_C_Edited_15_17.png)



<br>如果显示No Build System，大概率是编码或者格式问题，这个情况应该是自己再把配置编译系统的代码纯手敲一遍就可以解决。


## 配置Python环境

### 下载Python

- 前往[官网](https://www.python.org/downloads/windows/)下载并安装Python，这里以编辑此文时的最新版本Python为例，下载好并运行python.exe
- 没有什么特殊要求的话就点选Install Now，注意勾选Add Path，不过之后自己再去环境变量添加Path也行。安装好之后找到Python的路径。你可以通过菜单找到它的路径（配置编译系统的时候要用）
比如下面（注意斜杠）： 
```
C:/Users/IreneZ/AppData/Local/Programs/Python/Python310/python.exe
```

![图14-16](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_PY_Edited_1_4.png)


- 期间，你可以再在命令行敲Python看看是否安装成功

![图14-16](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_PY_5.png)




### 在Sublime里面运行Python


- 在Sublime Text 3新建配置一个Python3编译系统并保存，此处cmd用的就是刚刚安装Python时选择的路径


```
{
"cmd":["C:/Users/IreneZ/AppData/Local/Programs/Python/Python310/python.exe","-u","$file"],
"file_regex":"^[ ]File "(...?)", line ([0-9]*)",
"selector":"source.python",
} 
```

![图14-16](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_PY_Edited_6_7.png)



- 测试一下能不能用<br>
新建一个文件，编写Python代码，把右下角的Plain Text改为Python，选择Build System为刚刚配置的编译系统（例中是Python10），在Sublime Text 3中按快捷键Ctrl + B查看是否有结果输出

![图14-16](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/ST_PY_Edited_8_9.png)


## OK!