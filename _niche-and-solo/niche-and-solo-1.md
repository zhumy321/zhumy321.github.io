---
title:  如何使用算盘 # 
permalink: /niche-and-solo/1/
excerpt: "How to use an abacus" # 摘要，可不写
# author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
author_profile: false # 让作者信息从sidebar消失
last_modified_at: 2024-12-01T22:00:00+08:00 # 
# redirect_from:
#   - /theme-setup/
toc: true # true, false都可以
toc_label: "目录" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true # "Stick" table of contents to the top of a page. true: toc floats. false: toc fixed
words_per_minute: 200 # 经我实验，中文则将WPM设置为30为好
# 英文则设为200
sidebar:
  title: "自娱自乐"
  nav: sidebar-niche-and-solo # 这是在yaml文件里你要找到的那个导航栏的名字
---

缺2图

## 1. 算盘上的部件都怎么称呼？

首先，上拼多多买一个算盘。

<!-- 图在主力机里 -->

然后看下图

<!-- 图在主力机里 -->

拨珠法什么的就不介绍了，因为我不会，抱着会用即可、没必要处处仿古的心态，也没有认真学拨珠的方法。

<!-- 框、梁、档、珠四个基本部分组成。改进后的算盘又增加了清盘器、计位点和垫脚 -->

## 2. 算盘加减法


## 3. 算盘乘法

**学算盘算乘法前首先确保自己会背九九乘法表。**在这个前提下，可以用来运算乘法的方式有好几种，我只学了两种。其中，又觉得3.1这种比较方便。但不管是哪一种，都要先定位。定位的方法是：

假设有三个非零数字有以下关系

<!-- 这里可能加个表格会好懂一点 -->

ABC × DEF = GHIJKL

此处ABC称为实数，有m位（此处m=3）；DEF称为法数，有n位（此处n=3）；
GHIJKL称为积（可能有m+n位，也可能有m+n-1位）。“首”则是指这个数字的第一位，如实首就是指的数字A。

则定位有三种情况：

I. 若数字 A × D 要进位，则积首G会同时满足：G ≤ A 且 G ≤ D ，那么积的位数会等于 (m + n)。

如若 ABC × DEF = GHIJKL 对应 987 × 654 = 645498, 则 A × D = 6 × 9 = 54，是要进位的，那么此时的积645498的积首 G = 6 会同时满足 G ≤ A 且 G ≤ D 即 G ≤ 9 且 G ≤ 6 。积645498的位数等于 m + n = 6

II. 若数字 A × D 不进位，则除位齐的特殊情况外，积首G会同时满足：G ≥ A 且 G ≥ D ，那么积的位数会等于 (m + n - 1)。

如若 ABC × DEF = GHIJKL 对应 123 × 456 = 56088, 则 A × D = 1 × 4 = 4，不进位，那么此时的积56088的积首 G = 5 会同时满足G ≥ A 且 G ≥ D 即 G ≥ 1 且 G ≥ 4。积56088的位数等于 m + n - 1 = 5


III. 若数字 A × D 不进位，而发现 实首 = 法首 = 积首，即积首 G = A = D ，则要比较次高位是否满足I、II情况，以此类推。特殊情况“位齐”是指像100 × 100 = 10000，这种情况积的位数直接等于 (m + n - 1)。

如若 ABC × DEF = GHIJKL 对应 123 × 123 = 15129, 发现 积首 G = A = D，即 1 = 1 = 1 ，那么此时比较次高位 B、E与H。此处 B × E = 2 × 2 = 4，不进位，那么此时的积15129的次高位H为5， H = 5 同时满足H ≥ B 且 H ≥ E 即 H ≥ 2 且 H ≥ 2。积15129的位数等于 m + n - 1 = 5


### 3.1 空盘前乘法





### 3.2 破头后乘法

注意乘法口诀中的比如 1 × 6 = 6，我们在口算时可以背作一六得六，但是在用算盘时则要注意位一六**零六**，下面例子会体现这个用法规则。

如若 ABC × DEF 对应 183 × 825。

1. 将实数ABC拨入算盘，默记法数DEF。例中将183拨入算盘，默记825。![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Screenshot_20241201_1.jpg)

2. 实数的末位C与法数的首位D相乘，改变实数末位和实数末位的右一档。例中 C × D = 3 × 8 = 24，三八二十四，则**将C改为2**（这里是直接改，不用原来的末位1加上2），C的右边第一档由原来的空档改为4（其实是0 + 4 = 4 ）。![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Screenshot_20241201_2.jpg)

3. 依然是实数的末位C，现在与法数的次位E相乘，改变实数末位的右一档和右第二档，例中 C × E = 3 × 2 = 6，也就是三二零六，则将C的右一档（在第2步中拨为4的那一档）加上0，改为 4 + 0 = 4 ，C的右边第二档由原来的空档（也就是0）加上6，改为6。![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Screenshot_20241201_3.jpg)

4. 依然是实数的末位C，现在与法数的第三位F相乘，改变实数末位C的右边第二和右边第三档，例中 C × F = 3 × 5 = 15，也就是三五一十五，则将C的右边第二档（在第3步中拨为6的那一档）加上1，改为 6 + 1 = 7 ，C的右边第三档由原来的空档（也就是0）加上5，改为5。![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Screenshot_20241201_4.jpg)

5. 例中的法数总共只有三位，现在已经依次乘完了，则轮到实数的倒数第二位B与法数的首位D相乘，改变实数的倒数第二位（B位置）上的数字和实数末位（C位置）的数字。例中 B × D = 8 × 8 = 64，八八六十四，则**将B改为6**（这里是直接改，不用在原来的B位8加上6），实数末位C的位置上由原来的2（就是第1步中改为2的那一档）加上4，即2 + 4 = 6，这一档变为6。![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Screenshot_20241201_5.jpg)

6. 实数的倒数第二位B与法数的次位E相乘，改变实数B位右方的两档（即C和C右边那一档），例中 B × E = 8 × 2 = 16，也就是二八一十六，则将B的右一档（即C档）加上1，改为 6 + 1 = 7 ，B位置右方的第二档由原来的4加上6为10（这里进位了），也就是说这一档其实会变为0，刚刚改为7的B的右一档（即C档）现在又要加1变成8。![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Screenshot_20241201_6.jpg)

7. 现在实数的倒数第二位B与法数的末位F相乘，改变B右方第二档与右方第三档（即C位置的右边第一二档）。例中 B × F = 8 × 5 = 40，也就是五八四十，则将B的右边第二档（即C的右边第一档）加上4，再往右的一档加上0（相当于这档不变了）![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Screenshot_20241201_7.jpg)

8. 实数的第一位A与法数的首位D相乘，改变A右方的两档。注意一八零八，这个零的步骤不要略过了。然后是A与E（一二零二）、A与F（一五零五）结束后得到如下图。![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Screenshot_20241201_8.jpg)
![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Screenshot_20241201_9.jpg)


9. 以此类推，得到 183 × 825 = 150975 ![](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/Screenshot_20241201_10.jpg)



## 4. 算盘除法