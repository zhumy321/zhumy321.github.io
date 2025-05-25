---
title: 业余无线电手台功能说明 # 不写的话会从文件名自动生成。但标题不宜太长
permalink: /niche-and-solo/7/
excerpt: "泉盛UV K6为例" # 摘要，可不写
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
author_profile: false # 让作者信息从sidebar消失
last_modified_at: 2025-05-11T09:09:00+08:00 # 可不写，但layout则要写。+8是东八区
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


## 1-静噪等级 SQL

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_222629.png)

> 这个菜单项共有0、1、2...8、9共10个级别。代表的主要是接收信号的灵敏度。

如果是等级0、1这种，灵敏度就会很高，但也有时候，周围的噪声信号也会被收进来，如在家里开灯的时候会龇拉拉的；如果等级到8、9，电台就会静悄悄，要靠得非常近的时候才能解析到信号。所以模拟机一般静噪级别都比较低（比较灵敏）


## 2-步进频率 STEP

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_222537.png)

> 选项有2.5k、5k、6.25k、10K、12.5K、25K Hz。

这个是用来设定频率模式下的调节间隔。选为2.5k比较方便。如步进频率25kHz，则用上下键调频时，每次的间隔会是25kHz


## 3-发射功率 TXP

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_222431.png)

> 选项有高、中、低三种


VHF和UHF频段是无线电爱好者使用较为频繁和便利的频段，无论是在家里、车上或是旅行、工作中，都有U/V频段设备相伴。那么什么是U/V段呢？
UHF与VHF
VHF频带范围为，无线电波波长为10～1m，因此VHF又称为米波频带；UHF频带范围为300～3000MHz，无线电波长为1m～1dm，因此UHF又称为分米波频带。在无线电通信中，VHF是指甚高频段无线电波，其英文全称是VeryHighFrequency，中文简称为甚高频；UHF是指特高频段无线电波，其英文全称是UltraHighFrequency





如145.000频率段，这是V段的一个业余段，在离得近的地方，或者平常自己在家测试用，发射功率选低就可以了（省电）。这样子另外一台也能听得很清楚，如果远的话就选发射高功率。


### 如何区分U、V段？


| 分段 | 频率范围 | 备注 |
|------|---------|-----|
| 至低频(TLF) |    ＜3Hz        |  |
| 极低频(ELF) |    3-30Hz       |  |
| 超低频(SLF) |    30-300Hz     |  |
| 特低频(ULF) |    300-3000Hz   |  |
| 甚低频(VLF) |    3-30KHz      |  |
| 低频(LF)    |    30-300KHz    |  |
| 中频(MF)    |    300-3000KHz  |  |
| 高频(HF)    |    3-30MHz      |  |
| 甚高频(VHF) | 30-300MHz        |   50-54MHz、144-146MHz、146-148MHz为业余频段<br>其中144-146MHz为业余业务专用频段<br>144MHz: 波长2m   |
| 特高频(UHF) | 300-3000MHz | 430-440MHz、1240-1300MHz、2350-2450MHz为业余频段，且均为次要业务<br>波长70cm  |
| 超高频(SHF) | 3-30Ghz          |  |
| 极高频(EHF) | 30-300GHz        |  |
| 至高频(THF) | 300-3000GHz      |  |

> 许多国家（包括我们中国）的规范中，初级操作员只能使用V/U波段进行发射活动。V/U波段通信的一个特点是“视距通信”，即一般情况下通信距离取决于电台所在位置。只要双方天线之间没有高大建筑物或山地阻挡，小功率也可以实现远距离通信。

## 4-接收DCS R_DCS

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_222352.png)

> 选项有“无”和208个DCS代码（如D754I）

这个菜单是数字亚音频解码。

假设我的泉盛和宝锋都在同一个频率上，他们都不设亚音时可以互相听到。但若：

泉盛设置了接收DCS亚音，宝锋没有设置，那么泉盛叫宝锋，宝锋能听到的；然而宝锋叫泉盛，泉盛听不到（其实屏幕会显示信号，但是不解析声音）。

发射手台的发射DCS亚音和接收手台的接收DCS亚音一致，接收台才能接收到发射台的信号。这可以作为一种抗干扰的方式

## 5-接收CTCSS R_CTCS

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_222312.png)

> 选项有“无”和50个CTCSS亚音频率（如254.1Hz）

该菜单设置接收的CTCSS模拟亚音频率。模拟亚音也是一种抗干扰和识别的方式，只有在我的接收模拟亚音和对方（或中继台）的发射模拟亚音是同一个频率的时候，我才接收对方的信号或中继台才能把这个信号转发给我

## 6-发射DCS T_DCS

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_222215.png)

> 选项有“无”和208个DCS代码（如D754I）

略

## 7-发射CTCSS T_CTCS

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_221957.png)

> 选项有“无”和50个CTCSS亚音频率（如254.1Hz）

略。如果中继台设有指定的接收CTCSS，那么我的手台就要设置相应的发射CTCSS。


## 8-频差方向 SFT-D

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_221859.png)

> 选项有“+”、“-”和“无”

如中继接收各个从频率145.000（称上行频率）过来的信号，但是中继发出去给各个手台的频率一直是148.000（这个也称作中继的下行频率）。

——那也就是说我手台的屏幕上面显示当前的接收频率是148，但是我发射的频率得是145（即我，手台的发射频率比接收频率要低，叫做下差，是负号-）。

这里只选方向，具体频差的值是多少，要在下一菜单选


## 9-频差频率 OFFSET

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_221820.png)

我的手台在148上接收，145上发射，则是下差，频差频率绝对值为3MHz，方向则在上一菜单项设置。


## 10-宽窄带 W/N

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_221744.png)

> 选项有“宽”和“窄”这两项

一般默认是宽带（指对讲机在调频模式下，它的频带带宽是25kHz）—这种情况下5瓦的时候，在城区的工作范围大概有3~5公里，乡镇5-6公里。

选窄带则是将平台带宽设置为12.5kHz，这种情况下相同5瓦功率发射的时候，工作范围可以更远一些，城区5-6公里也是可以的。


## 11-加密通话Encode SCR

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_221711.png)

> 选项有“关”和1-10的加密级别

一般可能是频率，也可能是级别（如例中泉盛手台）。不管如何都要发射和接收的两方都用同样的加密方式才可以互相听到正常的话音。

但是正常情况下，作为业余电台，我们是要求明码通讯，不允许加密的。


## 12-繁忙禁发 BCL

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_221636.png)

> 只有“开”和“关”两个选项

如果我的手台打开了繁忙禁发，那么我正在接收信号的时候，我按自己的PTT键发射，是发不了东西出去的。


## 13-存储信道 MEM-CH

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_221545.png)

> 选项是信道数量（假设例中手台能支持存储200个信道，那这里面就会有200个选项）

首先回到频率模式，输入我指定的接收频率，然后设置好频差方向和频差频率，然后到存储信道功能项，选择存储到CH零零几，就可以了。

这个时候回到信道模式，就可以找到刚刚存储的00几信道了

## 14-省电模式 SAVE

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_221448.png)

> 选项有OFF和“1:1”、“1:2”、“1:3”、“1:4”。

默认是1:4。1:4的意思就是说把整个手台的待机时间分为4份，其中扫描信道的时间占1份，另外3份时间处于待机休眠状态。如果是OFF的话，手台就会连续守听，不遗漏任何一个信号，但会费电。


## 15-声控发射 VOX

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_221411.png)

> 选项有“关”和1-9的灵敏级别

如果这个功能是“关”，则只有在按下PTT键的时候才会发送我的话音。

如果打开（屏幕上也会显示VOX），则可以选择灵敏度，数字越低越灵敏，数字越高，越不容易误发射话音。这个依据环境音来调整。


## 16-亮屏设置 ABR

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_213537.png)

> 选项有“关”和数字1至5

数字是亮屏时间，单位是秒。

## 17-双守候 TDR


![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_213441.png)

> 选项有“关”和“信道A”、“信道B”这三个

正常在手台的显示界面，会有两组信道或者频率，上面是A信道，下面是B信道。

有实心箭头指着的那个信道，就是按PPT键将会发射的那一个信道，是默认工作的信道。

如果将此菜单设为选项“关”，就是把双守候关闭，则只有目前实心箭头指着的信道可以发射、接收，另外一个信道是不会去检测是否有信号过来的。

但如果在此菜单打开双守候的话（不论是设置成默认“信道A”还是“信道B”），两个信道都会去守，且**非默认的那一个信道过来信号时，及时按下PPT，可以即时在这个非默认信道上通话的。**<-注意，这个要和跨段收发做区分

## 18-跨段收发 WX

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_213400.png)

> 选项有“关”和“信道A”、“信道B”这三个

默认是“关”。

这个功能有点像双守候，但区别是跨段收发会强制使得信道A和B分别承担发射和接收的工作（从屏幕上看，实心箭头是本台发射的那一个信道）——也就是说，这个菜单项选择的是默认的发射信道，剩下的另一个没被选的就会默认为接收信道。


即，在双守候关闭、不做其他任何改动的情况下：

如果这个菜单项选择的是信道A，则默认用信道A（假设为145）来发射信号、用信道B（假设为438）来接收信号。有145的信号过来，手台收不到（**是否及时按PTT键都无法回复这个信号**），但438的信号过来是可以收到的。


## 19-按键音 BEEP

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_213313.png)

> 选项只有“开”和“关”两个

就是按按键的时候会不会“滴”。

## 20-发射限时 TOT

![Time Out Timer](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_213218.png)

> 选项有“关”和1-10min

一般默认是两分钟->按下PTT键2分钟后不管你有没有在说话，你的信号都不发射了。可以选择关闭或者其他的5分20分钟之类都的。

## 21-语音提示 VOICE

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_213130.png)

> 选项有“中文”、“ENG”和“关”

就是中英的语音，这个和菜单项50-语言选择在区别是50-语言选择设置的是显示界面的语言，这里21语音提示是语音的语言，不是同步的，所以要分别设置。

## 22-扫描模式 SC_REV

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_213049.png)

> 选项有CO, TO SE三种。

正常在显示界面发射的那一个信道，长按星号键就可以往后扫描，就可以知道目前你的附近有哪个频率在发射信号。

1. CO就是扫描到别人的信号后，会持续等在这个信号上，直到这个信号消失，才接着往后继续扫描。

2. TO就是扫描到别人的信号后，只等5秒钟（不管别人这个信号消不消失），如果5秒钟内你不做任何操作，它就会终止收听这个信号，然后接着往后扫描。

3. SE就是一旦扫描到别人的信号就会一直停留在这个信号上，不再扫描了。

## 23-信道显示模式 MDF

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_212956.png)

> 选项有“频率”、“信道名称”和“信道号”

默认是频率模式——就是在你的首页的时候，频率是最大最显眼的数字，信道是在它的旁边的小一点的数字。

如果改成其他选项，屏幕上最显眼的字就会是选中的那个选项（信道名称/信道号）

## 24-键盘自动锁定 AUTOLK

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_212901.png)

> 选项只有“开”和“关”

就是一段时间以后它是否自动锁屏。解锁的方式是长按井号键。

## 25-加入扫描1 S-ADD1

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250514_212813.png)




## 26-加入扫描2 S-ADD2

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_214604.png)

## 27-尾音消除 STE

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_214527.png)

> 选项只有“开”和“关”

对方手台说话说完、松开PTT的时候，我这边会听到有嚓的一声。

如果该菜单保持“关”，就会听到这个嚓声；

如果该菜单选择“开”，这个嚓的一声就会被消除。


## 28-中继确认 RP-STE


![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_214432.png)


> 选项有“关”和100ms到1000ms


默认情况下，此菜单为“关”——当我们向中继台按一下PTT键后松开，对面会回来一个信号（此时我的手台的绿灯也会亮）并“嚓”一声，这是提示我已能够与中继信号来回。

将该菜单设为非“关”以外的其他时间选项（比如最长的10\*100mS=1s），这个嚓应该就会消失了。

## 29-MIC灵敏度 MIC

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_214348.png)

> 选项有0、1、2、3、4共五个

麦克风话筒的灵敏度，总共有0、1、2、3、4这五个级别。泉盛UV K6默认是在2。

0的话，说话要靠近些，声音要大些，环境音带来的影响小一些。4的话，说话就可以距离远一些，诸如此类。

## 30-即呼信道 1-CALL

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_214309.png)



## 31-扫描列表选择 S-LIST

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_214208.png)


## 32-扫描列表1 SLIST1

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_214117.png)

## 33-扫描列表2 SLIST2

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_214032.png)

## 34-告警模式 AL-MOD

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_213945.png)

> 选项有远程、本地两种。

默认是远程模式。

远程：在其他机器（对方，数量可＞1）和本机（我）处于统一频率、两机可正常连接时，如出现紧急情况、无法发出话音，本机（我）长按告警键，其他机器（对方）会接收到信号并发出警笛声，此时即使本机（我）松手，告警依然会发送，直到本机（我）短按告警键，才会停止发送告警信号。

本地：跟频率上的其他机器没有关系，长按告警键，只有本机（我）会发出警笛声


## 35-本机身份码 ANI-ID

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_213902.png)

## 36-DTMF上线码 UPCODE

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_213825.png)

## 37-DTMF下线码 DWCODE

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_213736.png)

## 38-DTMF侧音开关 D-ST

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_213651.png)

## 39-DTMF呼叫响应 D-RSP

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250513_213608.png)


## 40-DTMF复位时间 D-HOLD

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_163052.png)

## 41-DTMF预载波 D-PRE

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_163013.png)

## 42-ANI发送模式 PTT-ID

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_162938.png)

## 43-DTMF解码开关 D-DCD

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_162902.png)

## 44-DTMF联系人 D-LIST

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_162830.png)

## 45-开机显示 PONMSG

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_162753.png)

> 选项有全显、电压、自定义字符

全显就是屏幕全亮，这个可以检查屏幕有没有坏点或者亮线。

电压就是手台当前的电池电压。

自定义符号需要连接到电脑来写入，可以放比如自己的呼号之类的。

## 46-发送结束音 ROGER

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_162718.png)

> 选项有蛙叫、嘀嘟和“无”

就是我向对方手台说话，当我松开PTT键的时候，我这边就没有声音输送过去了，但对方会听到我有一个结束音，提示我已经结束发送。这个声音就是此菜单选的蛙叫、嘀嘟。一般还是有个结束音较好。


## 47-电池电压 VOL

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_162645.png)


这个菜单没有选项，就是给你看看当前手台的电池电压是多少。

## 48-调制模式 MOD

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_162539.png)

## 49-NOAA接收模式 NOAA_S

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_162458.png)

## 50-语言选择 LANGUAGE

![语言选择](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_162415.png)

> 选项有“中文”和“ENG”


就是屏幕上显示的语言的选择。

## 51-删除信道 DEL-CH

![删除信道](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_162332.png)

## 52-复位 RESET

![复位](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Collage_20250511_162247.png)






<!-- 

## DTMF

438.500属于是u段的一个频率，要用v段频率的话直接输入v段就好了。

## 发射功率小于等于0.5瓦的设备不用执照

## 固定频段409-410兆赫兹内指定的20个频点可以不需要执照—409~410MHz是国际上通用的免执照频段。

## 有核准代码的，可以不需要执照。
 -->