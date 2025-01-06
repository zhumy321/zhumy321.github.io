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

### 原力觉醒
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-1-Begin.png)

### 与非门
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-2-NAND.png)

### 非门
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-3-NOT.png)

### 与门
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-4-1-AND.png)

### 或非门
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-4-2-NOR.png)

### 或门
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-4-3-OR.png)

### 高电平
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-5-Always-high.png)

### 第二刻
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-6-Second-second.png)


### 异或门
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-7-XOR.png)

### 三输入或门
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-8-1-Tri-OR.png)

### 三输入与门
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-8-2-Tri-AND.png)

### 同或门
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-9-XNOR.png)

### 成对的麻烦
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-10-2-Even-trouble.png)

| CD\\AB | 00 | 01 | 11 | 10  |
|:------:|:---:|:---:|:---:|:---:|
| 00     | 0  | 0  | 1  | 0   |
| 01     | 0  | 1  | 1  | 1   |
| 11     | 1  | 1  | 1  | 1   |
| 10     | 0  | 1  | 1  | 1   |

得到 Y = AB + AC + AD + BC + BD + CD

### 奇数个信号
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/TC-10-3-Odd-signal.png)


| CD\\AB | 00 | 01 | 11 | 10  |
|:------:|:---:|:---:|:---:|:---:|
| 00     | 0  | 1  | 0  | 1   |
| 01     | 1  | 0  | 1  | 0   |
| 11     | 0  | 1  | 0  | 1   |
| 10     | 1  | 0  | 1  | 0   |

化简后

| 右A⊕B；下C⊕D | 0 | 1 | 0 | 1  |
|:---------:|:---:|:---:|:---:|:---:|
| 0         | 0 | 1 | 0 | 1  |
| 1         | 1 | 0 | 1 | 0  |
| 0         | 0 | 1 | 0 | 1  |
| 1         | 1 | 0 | 1 | 0  |

得到 Y = (A ⊕ B) ⊕ (C ⊕ D)


### 