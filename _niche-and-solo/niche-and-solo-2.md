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

![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-11-2-Half-Adderl.png)


### 11-3 延迟线：略


### 12-1 加倍



## 处理器架构与可运行的计算机




## 编程


## 处理器架构2


## 函数


## 汇编挑战

