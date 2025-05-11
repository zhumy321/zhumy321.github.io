---
title: 三相电与TN系统 # 记得去导航栏加导航
permalink: /circuits-notes/circuits-notes-chinese-5/
excerpt: "" # 摘要，可不写
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
author_profile: false # 让作者信息从sidebar消失
last_modified_at: 2025-05-08T16:01:00+08:00 # 
# redirect_from:
#   - /theme-setup/
toc: true # true, false都可以
toc_label: "目录" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true # "Stick" table of contents to the top of a page. true: toc floats. false: toc fixed
words_per_minute: 200 # 经我实验，中文则将WPM设置为30为好
# 英文则设为200
sidebar:
  title: "sidebar-circuits-notes"
  nav: sidebar-circuits-notes # 这是在yaml文件里你要找到的那个导航栏的名字
---

## 三相电

其实发电站的产电过程非常原始，即使是核能、火力发电，也都是“烧开水”，高温高压的水蒸气驱动汽轮发电机组旋转（汽轮发电机组就是汽轮机和发电机同轴，这样3个为1组，共3个交流电流），发电机通过切割磁感线发电，产生的交流电经变压器升压后，就进入到电网，输电、配电后，就进入到千家万户。

这一组的3个交流电流处于相同的频率，但其波形的波峰和波谷偏移，以提供三个互补电流，相位分离为三分之一周期（120°或2π⁄3弧度）。发电机频率通常为 50Hz 或 60 Hz ，具体取决于国家或地区。[^1]

![3-phase flow](https://upload.wikimedia.org/wikipedia/commons/4/48/3-phase_flow.gif "三相电的电流流动")



## Why三相电

1. 因为单相交流电是由单个绕组的发电机输出的，其电压和功率随时间呈正弦波动，存在瞬时功率为零的时刻，导致能量传输不连续。这会造成电机振动、灯光闪烁等问题。而三个绕组的电压相位差为120°，其瞬时功率叠加后恒为常数（电压瞬时值之和则为0）。这是三相比单相或两相更核心的优势。

- **单相交流电**

> 其电压波形、电流波形（纯电阻负载时）、瞬时功率：

<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><mi>v</mi><mo stretchy="false">(</mo><mi>t</mi><mo stretchy="false">)</mo><mo>=</mo><msub><mi>V</mi><mi>m</mi></msub><mi>sin</mi><mo data-mjx-texclass="NONE">⁡</mo><mo stretchy="false">(</mo><mi>ω</mi><mi>t</mi><mo stretchy="false">)</mo></math>
<br>
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><mi>i</mi><mo stretchy="false">(</mo><mi>t</mi><mo stretchy="false">)</mo><mo>=</mo><msub><mi>I</mi><mi>m</mi></msub><mi>sin</mi><mo data-mjx-texclass="NONE">⁡</mo><mo stretchy="false">(</mo><mi>ω</mi><mi>t</mi><mo stretchy="false">)</mo></math>
<br>
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><mi>p</mi><mo stretchy="false">(</mo><mi>t</mi><mo stretchy="false">)</mo><mo>=</mo><mi>v</mi><mo stretchy="false">(</mo><mi>t</mi><mo stretchy="false">)</mo><mo>⋅</mo><mi>i</mi><mo stretchy="false">(</mo><mi>t</mi><mo stretchy="false">)</mo><mo>=</mo><msub><mi>V</mi><mi>m</mi></msub><msub><mi>I</mi><mi>m</mi></msub><msup><mi>sin</mi><mn>2</mn></msup><mo data-mjx-texclass="NONE">⁡</mo><mo stretchy="false">(</mo><mi>ω</mi><mi>t</mi><mo stretchy="false">)</mo></math>

> 当电压或电流过零点（即 ωt=0,π,2π,…）时，瞬时功率 𝑝(𝑡)=0。（最大值为Vm·Im）：

<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><msup><mi>sin</mi><mn>2</mn></msup><mo data-mjx-texclass="NONE">⁡</mo><mo stretchy="false">(</mo><mi>ω</mi><mi>t</mi><mo stretchy="false">)</mo><mo>=</mo><mfrac><mn>1</mn><mn>2</mn></mfrac><mo stretchy="false">[</mo><mn>1</mn><mo>−</mo><mo stretchy="false">(</mo><mn>2</mn><mi>cos</mi><mo data-mjx-texclass="NONE">⁡</mo><mi>ω</mi><mi>t</mi><mo stretchy="false">)</mo><mo stretchy="false">]</mo></math>

> 其实平常我们家用的220V插座供电的灯，亮度虽稳定（人眼无法察觉波动），但实际功率每秒有100次（50Hz系统）达到零值。

- **三相交流电**

<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><mrow data-mjx-texclass="INNER"><mo data-mjx-texclass="OPEN">{</mo><mtable columnalign="left left" columnspacing="1em" rowspacing=".2em"><mtr><mtd><msub><mi>V</mi><mi>A</mi></msub><mo stretchy="false">(</mo><mi>t</mi><mo stretchy="false">)</mo><mo>=</mo><msub><mi>V</mi><mi>m</mi></msub><mi>sin</mi><mo data-mjx-texclass="NONE">⁡</mo><mo stretchy="false">(</mo><mi>ω</mi><mi>t</mi><mo stretchy="false">)</mo></mtd></mtr><mtr><mtd><msub><mi>V</mi><mi>B</mi></msub><mo stretchy="false">(</mo><mi>t</mi><mo stretchy="false">)</mo><mo>=</mo><msub><mi>V</mi><mi>m</mi></msub><mi>sin</mi><mo data-mjx-texclass="NONE">⁡</mo><mo stretchy="false">(</mo><mi>ω</mi><mi>t</mi><mo>−</mo><mn>120</mn><mrow><mo>°</mo></mrow><mo stretchy="false">)</mo></mtd></mtr><mtr><mtd><msub><mi>V</mi><mi>C</mi></msub><mo stretchy="false">(</mo><mi>t</mi><mo stretchy="false">)</mo><mo>=</mo><msub><mi>V</mi><mi>m</mi></msub><mi>sin</mi><mo data-mjx-texclass="NONE">⁡</mo><mo stretchy="false">(</mo><mi>ω</mi><mi>t</mi><mo>+</mo><mn>120</mn><mrow><mo>°</mo></mrow><mo stretchy="false">)</mo></mtd></mtr></mtable><mo data-mjx-texclass="CLOSE" fence="true" stretchy="true" symmetric="true"></mo></mrow></math>

<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><mrow data-mjx-texclass="INNER"><mo data-mjx-texclass="OPEN">{</mo><mtable columnalign="left left" columnspacing="1em" rowspacing=".2em"><mtr><mtd><msub><mi>I</mi><mi>A</mi></msub><mo stretchy="false">(</mo><mi>t</mi><mo stretchy="false">)</mo><mo>=</mo><msub><mi>I</mi><mi>m</mi></msub><mi>sin</mi><mo data-mjx-texclass="NONE">⁡</mo><mo stretchy="false">(</mo><mi>ω</mi><mi>t</mi><mo>−</mo><mi>θ</mi><mo stretchy="false">)</mo></mtd></mtr><mtr><mtd><msub><mi>I</mi><mi>B</mi></msub><mo stretchy="false">(</mo><mi>t</mi><mo stretchy="false">)</mo><mo>=</mo><msub><mi>I</mi><mi>m</mi></msub><mi>sin</mi><mo data-mjx-texclass="NONE">⁡</mo><mo stretchy="false">(</mo><mi>ω</mi><mi>t</mi><mo>−</mo><mi>θ</mi><mo>−</mo><mn>120</mn><mrow><mo>°</mo></mrow><mo stretchy="false">)</mo></mtd></mtr><mtr><mtd><msub><mi>I</mi><mi>C</mi></msub><mo stretchy="false">(</mo><mi>t</mi><mo stretchy="false">)</mo><mo>=</mo><msub><mi>I</mi><mi>m</mi></msub><mi>sin</mi><mo data-mjx-texclass="NONE">⁡</mo><mo stretchy="false">(</mo><mi>ω</mi><mi>t</mi><mo>−</mo><mi>θ</mi><mo>+</mo><mn>120</mn><mrow><mo>°</mo></mrow><mo stretchy="false">)</mo></mtd></mtr></mtable><mo data-mjx-texclass="CLOSE" fence="true" stretchy="true" symmetric="true"></mo></mrow></math>

**θ 是负载的功率因数角（电压与电流的相位差）**

每相瞬时功率为电压与电流的乘积：
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><msub><mi>P</mi><mi>A</mi></msub><mo>=</mo><msub><mi>V</mi><mi>A</mi></msub><mo>⋅</mo><msub><mi>I</mi><mi>A</mi></msub></math>

总瞬时功率为三者之和：
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><msub><mi>P</mi><mrow><mi>t</mi><mi>o</mi><mi>t</mi><mi>a</mi><mi>l</mi></mrow></msub><mo>=</mo><msub><mi>P</mi><mi>A</mi></msub><mo>+</mo><msub><mi>P</mi><mi>B</mi></msub><mo>+</mo><msub><mi>P</mi><mi>C</mi></msub></math>

代入计算得到（计算过程待补充）

高频项抵消，总瞬时功率仅包含恒定的直流分量：
<math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><msub><mi>P</mi><mrow><mi>t</mi><mi>o</mi><mi>t</mi><mi>a</mi><mi>l</mi></mrow></msub><mo>=</mo><mn>3</mn><mo>⋅</mo><mfrac><mrow><msub><mi>V</mi><mi>m</mi></msub><msub><mi>I</mi><mi>m</mi></msub></mrow><mn>2</mn></mfrac><mo>⋅</mo><mi>cos</mi><mo data-mjx-texclass="NONE">⁡</mo><mi>θ</mi></math>

也就是说，
瞬时功率与时间无关、能量传输平稳（三相系统的总功率不再像单相系统那样存在脉动，始终稳定输出）。

2. 从物理结构上看，三个绕组对称分布时，转子受电磁力均匀，避免震动（两相绕组会造成转子受周期性力冲击）。

3. 稳定性上看，相数越多，平滑度越高：六相或十二相系统的瞬时功率更稳定，但收益增长微小（边际效益下降,系统复杂性）。

4. 材料效率上看，传输相同功率时，三相导线总截面积比单相节省约75%。单相需2根导线，三相需3根导线；相同传输功率下，三相导线电流更低，允许使用更细导线。

## 线电压、相电压与接线

![The basic 3-phase configurations](https://upload.wikimedia.org/wikipedia/commons/4/40/The_basic_3-phase_configurations_%28mul%29.svg "变压器接线")



- 线电压：两条相线（火线）之间的电压，用电压表测量任意两火线之间的压差，驱动三相负载工作的主要电压源

- 相电压：单条相线与中性点之间的电压，用电压表测量一火线与中性线间的压差，是单相设备的供电电压（如家用）


三相电在电源端和负载端均有星形和三角形两种接法。这2种接法都会有三条输电线(L1, L2, L3)及三个负载。而对于变压器，“三角形”连接的变压器绕组连接在三相系统的相之间。“星形”变压器将每个绕组从相线连接到公共中性点。要实现三相，可以使用单个三相变压器，也可以使用三个单相变压器。


### 星型(Y)接法

三相电的星形接法是将各相电源或负载的一端都接在一点上（这点就是中性点），对外则引出三条相线（L1/L2/L3），同时还可以将中性点引出作为中性线（N），形成三相四线制。也可不引出，形成三相三线制。当然，无论是否有中性线，都可以添加地线，分别成为三相五线制（L1/L2/L3+N+PE）或三相四线制(L1/L2/L3+N)。

用法：

星形接法的三相电，当三相负载均衡时，中性线电流为 0A；当负载不平衡时，中性线将有电流流过，来保持三相之间的平衡，以避免损坏电子设备——所以当三相负载不均衡时，必须接零线

- 在长距离传输中，仅用三根线来组成三相**三**线系统

- 电网在接入用户端一侧时往往会同时包含 220V 和 380V 电压输入，这时就需要三条相线和一条零线，构成三相**四**线制。

- 为了避免因泄漏导致的电压波动，用户需要增加一条地线。这样，三条相线、一条零线、一条地线构成了三相**五**线制。

线电压 = <svg xmlns="http://www.w3.org/2000/svg" width="3.061ex" height="2.398ex" viewBox="0 -996.8 1353 1060" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" style=""><defs><path id="MJX-2-TEX-N-221A" d="M95 178Q89 178 81 186T72 200T103 230T169 280T207 309Q209 311 212 311H213Q219 311 227 294T281 177Q300 134 312 108L397 -77Q398 -77 501 136T707 565T814 786Q820 800 834 800Q841 800 846 794T853 782V776L620 293L385 -193Q381 -200 366 -200Q357 -200 354 -197Q352 -195 256 15L160 225L144 214Q129 202 113 190T95 178Z"></path><path id="MJX-2-TEX-N-33" d="M127 463Q100 463 85 480T69 524Q69 579 117 622T233 665Q268 665 277 664Q351 652 390 611T430 522Q430 470 396 421T302 350L299 348Q299 347 308 345T337 336T375 315Q457 262 457 175Q457 96 395 37T238 -22Q158 -22 100 21T42 130Q42 158 60 175T105 193Q133 193 151 175T169 130Q169 119 166 110T159 94T148 82T136 74T126 70T118 67L114 66Q165 21 238 21Q293 21 321 74Q338 107 338 175V195Q338 290 274 322Q259 328 213 329L171 330L168 332Q166 335 166 348Q166 366 174 366Q202 366 232 371Q266 376 294 413T322 525V533Q322 590 287 612Q265 626 240 626Q208 626 181 615T143 592T132 580H135Q138 579 143 578T153 573T165 566T175 555T183 540T186 520Q186 498 172 481T127 463Z"></path></defs><g stroke="currentColor" fill="currentColor" stroke-width="0" transform="matrix(1 0 0 -1 0 0)"><g data-mml-node="math"><g data-mml-node="msqrt"><g transform="translate(853, 0)"><g data-mml-node="mn"><use xlink:href="#MJX-2-TEX-N-33"></use></g></g><g data-mml-node="mo" transform="translate(0, 136.7)"><use xlink:href="#MJX-2-TEX-N-221A"></use></g><rect width="500" height="60" x="853" y="876.8"></rect></g></g></g></svg> × 相电压  （约1.732倍）

线电流 = 相电流



![三相交流发电机接成星形电源连接星形负载](https://upload.wikimedia.org/wikipedia/commons/4/48/3_Phase_Power_Connected_to_Wye_Load.svg "三相交流发电机接成星形电源连接星形负载")


典型应用：

1. 电压220V的系统中：如中国民用电网（220V/380V）：火线(L)对中性线(N)为220V（相电压），火线间(L1、L2、L3互相之间)为380V（线电压）。

注意，我们平常说的 220V 单相交流电是指电压的有效值，（RMS，Root Mean Square）。等效于直流电220V的发热/做功能力的交流电压。


应用场景：

- 家庭插座取用L-N（220V）供家电使用；
- 三相电机直接接L-L（380V）驱动。


在电压110V的系统中，星形接法的线电压则为208v。


2. 欧洲工业系统（230V/400V）。



### 三角形(Δ)接法

三角形接法是在三相电系统中，一种连接电源或负载的方式，是将各相电源或负载依次首尾相连，并将每个相连的点引出，作为三相电的三个相线。三角形接法无中性点，也不可引出中性线，因此只有三相三线制。添加地线后，成为三相四线制。

线电压 = 相电压
（线电压即相电压本身。）

![](https://upload.wikimedia.org/wikipedia/commons/1/12/Delta_connection_currents.png "Y形配置的相量图，其中V ab表示线电压，V an表示相电压。")


典型应用：

1. 北美高压工业设备（如240V Δ系统）。

线电压（L1-L2）= 240V，同样等于相电压（绕组两端电压）。无中性线，无法直接获得更低的单相电压。

应用限制：需额外变压器提供单相电压（如120V）供照明和插座。


结构：其中一相绕组被中心抽头并接地，形成两个单相电压（如240V系统中抽头分120V+120V）。其他两相保持Δ连接。
线对地电压（以240V系统为例）：

L1-GND = 120V（低电压相）  
L2-GND = 208V（高脚相, 120V × √3）  
L3-GND = 120V（低电压相）  

兼容不同类型负载（120V单相设备 + 240V三相电机）；
高脚相（Wild Leg）需明确标识，避免误用于单相负载。


![High leg delta power system](https://solutioncenter.yaskawa.com/Platform/Publishing/images/CP_CE/1614373256948_High%20leg%20delta.jpg "中心抽头接地Delta系统")

> 这个系统也可能叫做以下名字 [^2]：
1. High leg delta power system （高脚Delta系统）
2. Split phase delta （裂相Delta）
3. Center grounded delta （中心抽头接地Delta系统）
4. Wild leg delta
5. Dog leg delta
6. Orange leg delta
7. Stinger leg delta
8. Four wire delta



2. 某些电机驱动场景（直接高电压供电）。



<!-- 记得补充 -->



## 汇总辨析

### 三相三线制(少用)

> 注：端线(End Line) = 火线(Live Line) = 活线(Active Line) = Phase (L1/L2/L3) = U/V/W = A/B/C

即只包括三相电的三个相线（A、B、C线，统称L，又称端线、火线、活线）。由于没有中性线（N线，又称中线、零线）和地线（PE线，又称接地线），这种供电方式**只能用于三相平衡负载**，且没有外壳接地保护。

三相供电若采取三相三线制，用户必须使用能平衡三相负载的电器，工厂则往往采用内部负载补偿的方法来达到总体三相负载平衡，地线则通过水管或避雷针连接至大地；**一般用电设备很少使用三相三线供电的方式，因为即使电器可以保证三相负载平衡，没有外壳接地保护也将对设备的安全使用造成巨大威胁。**

### 三相四线制

Y型的：三相四线制(L1/L2/L3+N)，不单独设地线（PE线），而是中性线和地线共用一条线路

Δ型的：三相四线制(L1/L2/L3+PE)

> 在一些平衡负载（如三相水泵），三相四线制指由三个相线和地线构成的系统（3P+E）。由于是三相平衡，即使是星形（Y型）接线也不需要中性线。

### 三相五线制

三相五线制包括三相电的三个相线（A、B、C线）、中性线（N线）以及地线（PE线）。地线在供电变压器侧和中性线并在一起，但进入用户侧后必须分开，否则发生混乱后就与三相四线制无异。



## TN系统(Terre-Neutre)

是国际电工委员会（IEC）定义的低压配电接地系统的一种，核心特点为：

- 电源中性点直接接地（直接连接大地）；
- 设备金属外壳通过保护导线（PE）与中性点连接，实现故障电流的低阻抗回流路径


根据中性线（N）与保护线（PE）是否共用导线，TN系统分为以下三种子类型：

1. TN-C 系统（N与PE合并为PEN线）

2. TN-S 系统（N与PE完全分离）

3. TN-C-S 系统（前半段合并为PEN线，后半段N与PE分离）


### TN-C系统：组合式中性与保护线

中性线（N）与保护线（PE）合并为PEN线，贯穿整个系统（电源端到负载端同一根导体）；
电源中性点接地，设备外壳直接连接PEN线。

电源中性点→PEN线→负载中性点  
            ↓  
          设备外壳


优点：

减少导线数量，节省成本；
适用于三相负载高度平衡的场景（如工业车间）。

缺点：

存在安全隐患：若PEN线断裂，断点后设备外壳可能带相电压（220V），引发触电风险；
PEN线同时承载工作电流和故障电流，易干扰精密设备。



应用场景

老式工业厂房（负载对称性好）；
已逐渐被淘汰，尤其禁止用于民用建筑。

### TN-S系统：完全分隔的中性与保护线

中性线（N）与保护线（PE）从电源端完全分离，全系统独立敷设；
电源中性点接地，设备外壳连接PE线。



电源中性点 → N线 → 负载中性点  
电源中性点 → PE线 → 设备外壳

优点：

安全性最高：PE线无工作电流，故障时电流路径明确，设备外壳电位接近零；
抗干扰能力强，适合精密仪器（如医疗设备、数据中心）。
缺点：

导线数量多（需单独敷设PE线），成本较高。


应用场景：

现代民用建筑（住宅、写字楼）；
对安全性要求高的场所（医院、实验室）。

### TN-C-S系统：分段合并与分离的混合模式
结构特点：

前半段（配电侧）：N与PE合并为PEN线；
后半段（负载侧）：PEN线在建筑物入口处分拆为独立的N线和PE线，后续不再合并。
示意图：

电源中性点→PEN线→建筑物入口→N线 → 负载中性点  
                      ↓  
                     PE线 → 设备外壳

优点：

经济性与安全性平衡：配电侧节省导线，用户侧保证安全；
兼容单相和三相机电设备。
缺点：

分断点后的PE线与N线必须严格绝缘，否则可能引发保护失效；
分断点处需进行重复接地以降低风险。
应用场景：

城乡结合部或农村电网（长距离供电成本敏感区域）；
大型商业综合体（配电侧高压，用户侧低压）。



这里没整理好,要记得回来补充




## 附表

### 各地区使用三相电的查找表

|  地区  | 连接方式 | 单相电压 | 三相电压  | 频率  |线的数量（不含地线）|
|:------:|----------|----------|--------|-------|------|
|  中国  | Y | 220V     | 380V  | 50Hz    | 3,4  |
|  中国台湾  | Δ | 110V     | 220/380V (相电压/线电压)     | 60Hz    | 4  |
|  日本  | Δ | 100V     | 200V  | 50/60Hz | 3  |
|  印度  | Y | 230V     | 400V  | 50Hz    |   |
| 俄罗斯 | Y | 127/220V | 380V  | 50Hz    |   |
|  德国  | Y | 220V     | 380V  | 50Hz    |   |
|  法国  | Y | 127/220V | 380V  | 50Hz    |   |
|  英国  | Y | 230V     | 415/480V     | 50Hz    |   |
| 意大利 | Y | 127/220V | 380V  | 50Hz    |   |
|  美国  | Δ | 120V     | 240/480V     | 60Hz    |   |
| 加拿大 | Δ || 120/208 V / 240 V / 480 V / 347/600 V   | 60 Hz   | 3, 4 |


## 参考资料

[^1]:[三相电] https://zh.wikipedia.org/wiki/%E4%B8%89%E7%9B%B8%E9%9B%BB 


[^2]:[Using a Drive on a High Leg Delta Power System] https://solutioncenter.yaskawa.com/selfservice/viewContent.do?externalId=13266&sliceId=1





