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

注意假设


## 例题一、入门的线性规划与代码解读

例题来自参考文献[1]

![线性规划问题1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/LinearProgramming-1.jpg)


### 假设


假设产品不积压，即产量等于销量

### 决策变量

这里最根源的变量应该是P1-P3这三种产品“分别要生产多少个”，这个数量如能确定，需要的原料的数量就能确定，加工的时间、销售后带来的利润也能确定。


### 目标函数

也就是说，设这三种产品的数量为决策变量x，即这三种产品分别生产x1, x2, x3个。三种产品各自带来的利润是常数，将这些常数其作为计算总利润的系数，则有总利润，也就是目标函数为

<!-- \max z = 70x_1 + 50x_2 + 60x_3 -->
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><mo data-mjx-texclass="OP" movablelimits="true">max</mo><mi>z</mi><mo>=</mo><mn>70</mn><msub><mi>x</mi><mn>1</mn></msub><mo>+</mo><mn>50</mn><msub><mi>x</mi><mn>2</mn></msub><mo>+</mo><mn>60</mn><msub><mi>x</mi><mn>3</mn></msub></math>

我们需要找到总利润的最大值；

### 约束条件

类似的，将每个产品的消耗的原材料作为系数，来计算消耗的每种原材料的总数，且令这个总数小于三种原材料分别的可用数量，则有约束条件

<!-- 
s.t.\begin{cases}2x_1 + 4x_2 + 3x_3 \le 150,
 \\ 3x_1 +  x_2 + 5x_3 \le 160,
 \\ 7x_1 + 3x_2 + 5x_3 \le 200,
 \\ x_i \ge 0, i = 1,2,3.
\end{cases}
 -->
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><mi>s</mi><mo>.</mo><mi>t</mi><mo>.</mo><mrow data-mjx-texclass="INNER"><mo data-mjx-texclass="OPEN">{</mo><mtable columnalign="left left" columnspacing="1em" rowspacing=".2em"><mtr><mtd><mn>2</mn><msub><mi>x</mi><mn>1</mn></msub><mo>+</mo><mn>4</mn><msub><mi>x</mi><mn>2</mn></msub><mo>+</mo><mn>3</mn><msub><mi>x</mi><mn>3</mn></msub><mo>≤</mo><mn>150</mn><mo>,</mo></mtd></mtr><mtr><mtd><mn>3</mn><msub><mi>x</mi><mn>1</mn></msub><mo>+</mo><msub><mi>x</mi><mn>2</mn></msub><mo>+</mo><mn>5</mn><msub><mi>x</mi><mn>3</mn></msub><mo>≤</mo><mn>160</mn><mo>,</mo></mtd></mtr><mtr><mtd><mn>7</mn><msub><mi>x</mi><mn>1</mn></msub><mo>+</mo><mn>3</mn><msub><mi>x</mi><mn>2</mn></msub><mo>+</mo><mn>5</mn><msub><mi>x</mi><mn>3</mn></msub><mo>≤</mo><mn>200</mn><mo>,</mo></mtd></mtr><mtr><mtd><msub><mi>x</mi><mi>i</mi></msub><mo>≥</mo><mn>0</mn><mo>,</mo><mi>i</mi><mo>=</mo><mn>1</mn><mo>,</mo><mn>2</mn><mo>,</mo><mn>3.</mn></mtd></mtr></mtable><mo data-mjx-texclass="CLOSE" fence="true" stretchy="true" symmetric="true"></mo></mrow></math>


### 代码实现

```
# -*- coding: utf-8 -*-
import cvxpy as cp
from numpy import array

# linear-program_v1.0：last changed on 2025.08.03
# changes: 1st release
# author: Irene ZHU

print('\n 线性规划: \n')
print(' 1. 寻找决策变量x_i\n')
print(' 2. 考虑包含非负约束在内的所有约束条件，约束条件称constraints\n')
print(' 3. 构造关于决策变量(x_i)的一个线性函数，称目标函数objective function\n')
print(' 4. 数学规划模型一定要做灵敏度分析！\n\n')
print('  ***  以上是说明 *** \n\n')

## 第一种写法
### 1. 决策变量x1, x2, x3

x1 = cp.Variable()  # 定义连续变量
'''
cp.Variable()函数的说明：
不带任何参数时：创建一个标量连续实数变量(默认浮点型)
如果带整型参数：cp.Variable(integer=True)创建整数变量
如果带布尔参数：cp.Variable(boolean=True)创建布尔变量
如果带非负约束：x_nonneg = cp.Variable(nonneg=True)
'''
x2 = cp.Variable() 
x3 = cp.Variable() 

### 2. 约束条件

constraints = [ 2*x1+4*x2+3*x3<=150,
        3*x1+x2+5*x3<=160,
        7*x1+3*x2+5*x3<=200,
        x1>=0,
        x2>=0,
        x3>=0,] # 定义约束条件
# 约束条件也可以是等式，如x1+x2==10000

### 3. 目标函数

objective = cp.Maximize(70*x1+50*x2+60*x3) # 定义目标函数
# 如求最小值则是cp.Minimize

prob = cp.Problem(objective, constraints) # 创建一个优化问题的实例

prob.solve(verbose=True)  # 开启详细输出和求解刚才创建的这个实例问题
'''
prob.solve()函数的说明：
它会自动选择适合的凸优化求解器(如ECOS, SCS等)进行数值计算
求解过程包含：验证问题的凸性、
将问题转化为标准形式、调用数值优化算法、计算最优解
'''

print('\n\n目标函数的最优值: ',prob.value)

print('x1: ', x1.value)
print('x2: ', x2.value)
print('x3: ', x3.value)



'''
## 第二种写法
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


```

解得

```
目标函数的最优值:  2590.909090524814
x1:  8.351846141345627
x2:  21.988209753513253
x3:  15.114489549249292
[Finished in 747ms]
```


### 灵敏度分析

待补充


## 例题二、稍进阶的线性规划与代码解读


![线性规划问题1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/LinearProgramming-2.jpg)

### 假设

运输过程中不产生产品损耗

### 决策变量

例中有6个产地，8个销售地，从不同产地到不同销售地的运费各不相同，可以将B1地需求全部由A1供应，也可以将B1地需求由A1-A5五处共同满足。最终需要找到的是运费最少的方案。也就是说，需要明确，6个产地分别发出多少商品到8个销售地，如：

对A1来说，要往B1运输X11个产品、往B2地运输X12个产品...往B8地运输X18个产品

...

对A6来说，要往B1地运输X61个产品，往B2地运输X62个产品...往B8地运输X88个产品。

这样，未知数X总共有48个，需要找到最合适的48个数量，使得最终的运费最低。这里可以在代码实现的时候使得X为一个6行8列的矩阵。


### 约束条件

每个产地的产量是有限的，每个销售地的需求也是有限的，在总产量大于总需求的情况下，要让每个销售地区的需求都得到满足。也就是说，如对于B3地，销量是22，那么从6个产地送过来的总数量要等于22，即 X13+X23+X33+X43+X53+X63=22

### 目标函数

题目表中6行8列的数字是单位运费，可以视作一个6行8列的矩阵；而决策变量的48个X也已经计划用6行8列的矩阵来表示，因此这两个矩阵的形状是相同的。

这两个矩阵中，在相同位置的2个元素相乘（运费单价\*运送数量），就会得到一个新的6行8列的矩阵（假设是Y），那么新矩阵的每个元素就是一条运输路线上的总运费（如元素Y11是从A1地运输X11个产品到B1地的总运费）。那么，总的运费就是新的矩阵Y的所有元素的和。


### 代码实现

```
# -*- coding: utf-8 -*-
import cvxpy as cp
import numpy as np

# linear-program-2_v1.0：last changed on 2025.08.03
# changes: 1st release
# author: Irene ZHU

print('\n 线性规划: \n')
print(' 1. 寻找决策变量x_i\n')
print(' 2. 考虑包含非负约束在内的所有约束条件，约束条件称（s.t.=subject to）constraints\n')
print(' 3. 构造关于决策变量(x_i)的一个线性函数，称目标函数objective function\n')
print(' 4. 数学规划模型一定要做灵敏度分析！\n\n')
print('  ***  以上是说明 *** \n\n')

### 1. 决策变量x

'''
cp.Variable()
不带任何参数时：创建一个标量连续实数变量(默认浮点型)
如果带整型参数：cp.Variable(integer=True)创建整数变量
如果带布尔参数：cp.Variable(boolean=True)创建布尔变量
如果带非负约束：x_nonneg = cp.Variable(nonneg=True)
如果是严格为正的标量变量：cp.Variable(pos=True)
'''
# 创建变量矩阵 (6行8列的二维矩阵)
x = cp.Variable((6, 8), nonneg=True, integer=True) 
# 如果x可以是小数，去掉参数integer=True即可


### 2. 约束条件

# 创建系数矩阵 (6行8列的二维矩阵)
coefficient_matrix = np.array([
    [6, 2, 6, 7, 4, 2, 5, 9],
    [4, 9, 5, 3, 8, 5, 8, 2],
    [5, 2, 1, 9, 7, 4, 3, 3],
    [7, 6, 7, 3, 9, 2, 7, 1],
    [2, 3, 9, 5, 7, 2, 6, 5],
    [5, 5, 2, 2, 8, 1, 4, 3]
])

'''
# 验证一下，别搞错行列数了
print('第一行数字是')
print(coefficient_matrix[0]) # 让索引为0，看一下第一行

print('第一列数字是')
print(coefficient_matrix[:,0]) # 让索引为0，看一下第一列
'''

# 从每个产地运出的商品总数要小于等于每行的产量：

row_sums = cp.sum(x, axis=1) # 6个产地发出产品
row_limits = np.array([60, 55, 51, 43, 41, 52])  # 这是上限，row_sums要小于row_limits
# cp.sum(矩阵, axis=1) 函数的说明：
# 它会对指定矩阵的每一行元素求和，
# 最终得到一个与这个矩阵行数相同但只有1列的向量
# 其中每个元素是原来新矩阵每行所有元素的乘积和
# 这里row_sums就是一个6行1列的向量，


# 从每个产地运到销售地的商品总数要等于销售地的需求量：

col_sums = cp.sum(x, axis=0)
col_limits = np.array([35, 37, 22, 32, 41, 32, 43, 38])  # row_sums要等于row_limits


# 构建优化实例
constraints = [
    x >= 0,
    row_sums <= row_limits, # 这里是行列相同的向量，会自动根据位置比较大小
    col_sums == col_limits     
]


### 3. 目标函数

# 正确写法
Y = cp.multiply(x, coefficient_matrix)  
# cp.multiply(矩阵1, 矩阵2)是元素级乘法（Hadamard积），是2个同样形状的矩阵逐元素相乘（对应位置相乘）得到一个同样形状的新矩阵
# c = x * coefficient_matrix这个写法在CVXPY里面可能会出问题，所以这里不这么写

objective = cp.Minimize(cp.sum(c)) # 定义目标函数
# 如求最大值则是cp.Maximize

prob = cp.Problem(objective, constraints) # 创建一个优化问题实例

prob.solve(verbose=True)  # 开启详细输出
# 求解刚才创建的这个实例问题
'''
prob.solve()函数的说明：
它会自动选择适合的凸优化求解器(如ECOS, SCS等)进行数值计算
求解过程包含：验证问题的凸性、
将问题转化为标准形式、调用数值优化算法、计算最优解
'''

print('\n\n目标函数的最优值: ',prob.value)

print('\n变量x的取值矩阵:')
print(np.round(x.value, 4))  # 保留4位小数


```


解得：


```
目标函数的最优值:  664.0

变量x的取值矩阵:
[[-0. 19. -0. -0. 41. -0. -0. -0.]
 [-0. -0. -0. 32. -0. -0. -0.  1.]
 [-0. 12. 22. -0. -0. -0. 17. -0.]
 [-0. -0. -0. -0. -0.  6. -0. 37.]
 [35.  6. -0. -0. -0. -0. -0. -0.]
 [-0. -0. -0. -0. -0. 26. 26. -0.]]
[Finished in 871ms]
```

![线性规划问题1](https://raw.githubusercontent.com/zhumy321/diy-imagehost/main/img/LinearProgramming-3.jpg)

### 灵敏度分析

待补充

### 为什么这题我最开始算错——决策变量

因为决策变量搞糊涂了。

题目表中6行8列的数字是单位运费，

但是写代码太上头，忘记了这回事，渐渐地把题目表中6行8列的数字当成了运出的数量，写成了如下代码：

```

# 计算每行的加权和 (得到6个值)
row_sums = cp.sum(cp.multiply(coefficient_matrix, x), axis=1)
# 把coefficient_matrix当成了运输数量（实际上是运输单价）
row_limits = np.array([60, 55, 51, 43, 41, 52])  


# 计算每列的加权和 (得到8个值)
col_sums = cp.sum(cp.multiply(coefficient_matrix, x), axis=0)
col_limits = np.array([35, 37, 22, 32, 41, 32, 43, 38])  

# 构建优化实例
constraints = [
    x >= 0,
    row_sums <= row_limits,   
    col_sums == col_limits    
]

# 这套计算式下，
# row_sums其实是每个产地发出的货物的总运费，让它小于每个产地的产量row_limits，是毫无逻辑的；
# col_sums则是每个销售地收到的货物的总运费，让它等于每个销售地的销量col_limits，也是没道理的。
```

这套计算式下，

row_sums其实是每个产地发出的货物的总运费，让它小于每个产地的产量row_limits，是毫无逻辑的；

col_sums则是每个销售地收到的货物的总运费，让它等于每个销售地的销量col_limits，也是没道理的。

这相当于模型的逻辑全乱套了。

所以一定要时时刻刻明确决策变量的物理意义。


## 例题三、整数规划




## 参考文献

[1] 司守奎, 孙玺菁. Python数学建模算法与应用[M]. 北京: 国防工业出版社. 2022年1月第一版第一次印刷.
