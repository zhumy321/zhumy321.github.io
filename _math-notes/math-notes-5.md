---
title:  线性规划 # 
permalink: /math-notes/math-notes-chinese-5/
excerpt: "" # 摘要，可不写
# author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
author_profile: false # 让作者信息从sidebar消失
last_modified_at: 2025-04-17T23:00:00+08:00 # 
# redirect_from:
#   - /theme-setup/
toc: true # true, false都可以
toc_label: "目录" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true # "Stick" table of contents to the top of a page. true: toc floats. false: toc fixed
words_per_minute: 200 # 经我实验，中文则将WPM设置为30为好
# 英文则设为200
sidebar:
  title: "sidebar-math-notes"
  nav: sidebar-math-notes # 这是在yaml文件里你要找到的那个导航栏的名字
---


## 例1

### 原题

！本例来自《Python数学建模算法与应用》——...markdown增加引用。增加题目

求解

<!-- \max z = 70x_1 + 50x_2 + 60x_3 -->
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><mo data-mjx-texclass="OP" movablelimits="true">max</mo><mi>z</mi><mo>=</mo><mn>70</mn><msub><mi>x</mi><mn>1</mn></msub><mo>+</mo><mn>50</mn><msub><mi>x</mi><mn>2</mn></msub><mo>+</mo><mn>60</mn><msub><mi>x</mi><mn>3</mn></msub></math>

<!-- 
s.t.\begin{cases}2x_1 + 4x_2 + 3x_3 \le 150,
 \\ 3x_1 +  x_2 + 5x_3 \le 160,
 \\ 7x_1 + 3x_2 + 5x_3 \le 200,
 \\ x_i \ge 0, i = 1,2,3.
\end{cases}
 -->
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><mi>s</mi><mo>.</mo><mi>t</mi><mo>.</mo><mrow data-mjx-texclass="INNER"><mo data-mjx-texclass="OPEN">{</mo><mtable columnalign="left left" columnspacing="1em" rowspacing=".2em"><mtr><mtd><mn>2</mn><msub><mi>x</mi><mn>1</mn></msub><mo>+</mo><mn>4</mn><msub><mi>x</mi><mn>2</mn></msub><mo>+</mo><mn>3</mn><msub><mi>x</mi><mn>3</mn></msub><mo>≤</mo><mn>150</mn><mo>,</mo></mtd></mtr><mtr><mtd><mn>3</mn><msub><mi>x</mi><mn>1</mn></msub><mo>+</mo><msub><mi>x</mi><mn>2</mn></msub><mo>+</mo><mn>5</mn><msub><mi>x</mi><mn>3</mn></msub><mo>≤</mo><mn>160</mn><mo>,</mo></mtd></mtr><mtr><mtd><mn>7</mn><msub><mi>x</mi><mn>1</mn></msub><mo>+</mo><mn>3</mn><msub><mi>x</mi><mn>2</mn></msub><mo>+</mo><mn>5</mn><msub><mi>x</mi><mn>3</mn></msub><mo>≤</mo><mn>200</mn><mo>,</mo></mtd></mtr><mtr><mtd><msub><mi>x</mi><mi>i</mi></msub><mo>≥</mo><mn>0</mn><mo>,</mo><mi>i</mi><mo>=</mo><mn>1</mn><mo>,</mo><mn>2</mn><mo>,</mo><mn>3.</mn></mtd></mtr></mtable><mo data-mjx-texclass="CLOSE" fence="true" stretchy="true" symmetric="true"></mo></mrow></math>

### 分析





### 解法1

程序较简单，好写好懂，不易出错

```
import cvxpy as cp

from numpy import array

x1 = cp.Variable()  # 定义连续变量
x2 = cp.Variable() 
x3 = cp.Variable() 

objective = cp.Maximize(70*x1+50*x2+60*x3) # 定义目标函数

constraints = [ 2*x1+4*x2+3*x3<=150,
                3*x1+x2+5*x3<=160,
                7*x1+3*x2+5*x3<=200,
                x1>=0,
                x2>=0,
                x3>=0,] # 定义约束条件

prob = cp.Problem(objective, constraints) # 创建优化问题

prob.solve() # 求解问题

print('最优值: ',prob.value)

print('x1: ', x1.value)
print('x2: ', x2.value)
print('x3: ', x3.value)


'''
最优值: 2590.909090524814
x1:  8.351846141345627
x2:  21.988209753513253
x3:  15.114489549249292

'''

```

### 解法2

精简，但是需要熟练，不然容易出错

```
import cvxpy as cp

from numpy import array
c = array([70, 50, 60]) # 定义目标向量

a = array([[2,4,3], [3,1,5], [7,3,5]])  # 定义约束矩阵

b = array([150, 160, 200]) # 定义约束条件的右边向量

x = cp.Variable(3, pos=True) # 定义3个决策变量

obj = cp.Maximize(c@x) # 构造目标函数。@是矩阵乘法的乘号

cons = [ a@x <= b] # 构造约束条件。注意是[]

prob = cp.Problem(obj, cons) # 创建优化问题

prob.solve() # 求解问题

print('最优值: ',prob.value)

print('最优解: ', x.value)


'''
最优值: 2590.909090524814
最优解: [ 8.35184614 21.98820975 15.11448955]
'''

```


