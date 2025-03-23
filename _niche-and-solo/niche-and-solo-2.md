---
title: 游戏*Turing Complete*与数字电路 # 
permalink: /niche-and-solo/2/
excerpt: "Look into the game Turing Complete" # 摘要，可不写
author_profile: false # 让作者信息从sidebar消失
last_modified_at: 2024-12-01T22:00:00+08:00 # 
toc: true # true, false都可以
toc_label: "目录" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true # "Stick" table of contents to the top of a page. true: toc floats. false: toc fixed
words_per_minute: 200 
sidebar:
  title: "自娱自乐"
  nav: sidebar-niche-and-solo # 这是在yaml文件里你要找到的那个导航栏的名字
---

## 基础逻辑

### 1 原力觉醒

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-1-Begin.png)

### 2 与非门

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-2-NAND.png)

### 3 非门

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-3-NOT.png)

### 4-1 与门

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-4-1-AND.png)

### 4-2 或非门

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-4-2-NOR.png)

### 4-3 或门

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-4-3-OR.png)

### 5 高电平

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-5-Always-high.png)

### 6 第二刻

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-6-Second-second.png)

### 7 异或门

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-7-XOR.png)

### 8-1 三输入或门

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-8-1-Tri-OR.png)

### 8-2 三输入与门

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-8-2-Tri-AND.png)

### 9 同或门

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-9-XNOR.png)

## 算术运算与存储器

### 10-1 二进制速算：略

### 10-2 成对的麻烦

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-10-2-Even-trouble.png)

| CD\\AB | 00 | 01 | 11 | 10  |
|:------:|:---:|:---:|:---:|:---:|
| 00     | 0  | 0  | 1  | 0   |
| 01     | 0  | 1  | 1  | 1   |
| 11     | 1  | 1  | 1  | 1   |
| 10     | 0  | 1  | 1  | 1   |

得到 Y = AB + AC + AD + BC + BD + CD

### 10-3 奇数个信号

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-10-3-Odd-signal.png)


| CD\\AB | 00 | 01 | 11 | 10  |
|:------:|:---:|:---:|:---:|:---:|
| 00     | 0  | 1  | 0  | 1   |
| 01     | 1  | 0  | 1  | 0   |
| 11     | 0  | 1  | 0  | 1   |
| 10     | 1  | 0  | 1  | 0   |

化简后

| 下方C⊕D\\右A⊕B | 0 | 1 | 0 | 1  |
|:---------:|:---:|:---:|:---:|:---:|
| 0         | 0 | 1 | 0 | 1  |
| 1         | 1 | 0 | 1 | 0  |
| 0         | 0 | 1 | 0 | 1  |
| 1         | 1 | 0 | 1 | 0  |

得到 Y = (A ⊕ B) ⊕ (C ⊕ D)

### 10-4 循环依赖：略


### 11-1 信号计数

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-11-1-Signal-Counting.png)

| CD\\AB | 00 | 01 | 11 | 10  |
|:------:|:---:|:---:|:---:|:---:|
| 00     | 0  | 1  | 2  | 1   |
| 01     | 1  | 2  | 3  | 2   |
| 11     | 2  | 3  | 4  | 3   |
| 10     | 1  | 2  | 3  | 2   |

最后输出的三个比特分别是上、中、下比特，则

上：

| CD\\AB  | 00 | 01 | 11 | 10  |
|----|----|----|----|-----|
| 00 |    | 1  |    | 1   |
| 01 | 1  |    | 1  |     |
| 11 |    | 1  |    | 1   |
| 10 | 1  |    | 1  |     |

上 = (A ⊕ B) ⊕ (C ⊕ D)

中：

| CD\\AB  | 00 | 01 | 11 | 10  |
|----|----|----|----|-----|
| 00 |    |    | 1  |     |
| 01 |    | 1  | 1  | 1   |
| 11 | 1  | 1  |    | 1   |
| 10 |    | 1  | 1  | 1   |

中 = AB(~C)+A(~B)D+AC(~D)+(~A)BD+(~A)CD+(~A)BC

下：

| CD\\AB  | 00 | 01 | 11 | 10  |
|----|----|----|----|-----|
| 00 |    |    |    |     |
| 01 |    |    |    |     |
| 11 |    |    | 1  |     |
| 10 |    |    |    |     |


下 = ABCD


### 11-2 半加器

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-11-2-Half-Adder.png)

| AB  | 00 | 01 | 11 | 10  |
|-----|----|----|----|-----|
| SUM | 0  | 1  | 0  | 1   |

SUM = A⊕B


| AB  | 00 | 01 | 11 | 10  |
|-----|----|----|----|-----|
| CAR | 0  | 0  | 1  | 0   |

CAR = AB

### 11-3 延迟线：略


### 12-1 加倍

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-12-1-Double.png)


### 12-2 全加器

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-12-2-Full-Adder-1.png)


### 12-3 奇变偶不变

缺


### 13-1 1位开关

缺

### 13-2 1位取反器

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-13-2-one_bit_inverter_that_is_xor.png)


### 14-1 8位或

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-14-1-8bit_or_1.png)
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-14-1-8bit_or_2.png)


### 14-2 8位非


### 14-3 8位加法器


### 15-1 负数



### 15-2 数据选择器


### 16-1 相反数


### 16-2 总线


### 16-3 优雅存储




### 17 存储1字节

### 18 1位解码器


### 19 3位解码器


### 20-1 逻辑引擎



### 20-2 小盒子

### 20-3 计数器






## 处理器架构与可运行的计算机


### 21-1 算数引擎


### 21-2 寄存器之间

### 23 元件工坊

### 24 指令解码器

### 25 计算单元


### 26-1 条件判断

### 26-2 程序

### 27 立即数

### 28 图灵完备-可运行的计算机

## 编程


### 29 加5等于几


### 30 激光炮直瞄



### 30-1 太空入侵者


### 30-2 密码锁


### 30-3 时间掩码


### 31 迷宫

## 处理器架构2


### 32-1 异或



### 32-2 8位常数



### 33-1 8位异或



### 33-2 相等



### 34-1 无符号小于

### 34-2 有符号小于

### 35 宽指令

### 36 一把线，像挂面


### 37 操作码

### 38 立即数

### 39 条件判断



## 函数

### 40-1 16进制速算


### 40-2 移位
### 40-3 随机存储器
### 40-4延迟量


### 41-1 半字节乘法

### 41-2 栈

### 41-3 实验室

### 42-1 除法

### 42-2 压栈与弹栈

### 43 函数

## 汇编挑战

### 44-1 AI打牌

### 44-2 机器赛跑

### 44-3 新品上市

### 44-4 美味排序



### 45-1 跳舞机器


### 45-2 核金汉诺塔

### 45-3 行星之名


### 46 水世界
