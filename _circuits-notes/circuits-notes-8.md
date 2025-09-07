---
title: 全球各地储能政策-2025-Sept-Irene # 记得去导航栏加导航
permalink: /circuits-notes/circuits-notes-chinese-8/
excerpt: "全文由本站作者单独整理编写。" # 摘要，可不写
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
author_profile: true # 让作者信息从sidebar消失
last_modified_at: 2025-09-07T09:19:00+08:00 # 
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

<!-- 


## AS3000
https://www.standardsau.com/preview/AS%20NZS%203000-2018.pdf


# 总论

https://www.energy.gov.au/about-site

 -->

## 1. 澳大利亚

### 1.1 适用澳大利亚全境的SRES计划（小系统）
SRES：[Small-scale renewable energy systems](https://cer.gov.au/schemes/renewable-energy-target/small-scale-renewable-energy-scheme/small-scale-renewable-energy-systems)

该计划下包含6种类型：
- 太阳能电池
- 太阳能光伏（PV）
- 风力涡轮机
- 水力系统
- 太阳能热水器
- 空气源热泵

**补贴形式** ：小规模技术证书: Small-scale Technology Certificates (STCs)

**STC 的来源**：用户安装或升级屋顶太阳能系统时，会获得一定数量的 STC，与太阳能零售商/认证安装商签订合同后，用户 STC 的所有权即转让给商家，此时商家把折扣兑换给用户。

**STC 的价值**：取决于**用户安装的太阳能系统到 2030 年预计产生的电量**，具体到金额，则取决于以下条件：
- 太阳能系统的规模（kw）（最大 100 kw）
- 安装该系统的气候区。
通常情况下，STCs的交易价格约为40澳元（[此价格存在波动](https://solarcalculator.com.au/battery-storage/rebate/)）。扣除行政费用后，实际价值约为37澳元。

![STC-Zones-in-Australia-as-of-1st-January-2019.jpg (1399×818)](https://www.solarchoice.net.au/wp-content/uploads/STC-Zones-in-Australia-as-of-1st-January-2019.jpg)


**对太阳能光伏、太阳能电池、风能或水力发电系统**，有如下要求：

- 在安装后 12 个月内创建 STC
- 其面板、电池或逆变器已列入[清洁能源委员会 (CEC) 批准的组件清单](https://www.cleanenergycouncil.org.au/industry/products)
- 符合澳大利亚和新西兰标准
- [由获得澳大利亚太阳能认证协会 (SAA) 认可的、](https://saaustralia.com.au/accreditation-status-check/)适合该安装类型的设计师和安装人员进行设计和安装
- 符合[SAA 设计和安装指南](https://saaustralia.com.au/about-accreditation/)
- 遵守所有地方、州、领地和联邦的要求，包括电气安全
- 被归类为小规模。

**对太阳能热水器系统和空气源热泵**，有如下要求：

- 列入[太阳能热水器登记册](https://cer.gov.au/schemes/renewable-energy-target/small-scale-renewable-energy-scheme/small-scale-renewable-energy-systems/solar-water-heaters/register-solar-water-heaters "太阳能热水器登记册")
- 在安装后 12 个月内创建 STC

#### 1.1.1 **太阳能电池补贴 = Cheaper Home Batteries Program**

[Cheaper Home Batteries Program](https://www.dcceew.gov.au/energy/programs/cheaper-home-batteries)
[概述]([太阳能电池 |清洁能源调节器](https://cer.gov.au/schemes/renewable-energy-target/small-scale-renewable-energy-scheme/small-scale-renewable-energy-systems/solar-batteries))
于2025 年 7 月 1 日施行，取代原有的电池相关政策（如维多利亚州的8,800 美元免息贷款），预计于2030年12月31日结束。2025-2030年之间的激励会逐年减少。


| 项目       | 返利金额   | 申请人资质               | 简要说明                       |
| -------- | ------ | ------------------- | -------------------------- |
| 廉价家用电池计划 | 最高约30% | 房主、小型企业、社区设施，不设收入门槛 | 电池系统必须符合项目标准。补贴可以与太阳能板补贴叠加 |


**申请条件**
- 电池容量需在5-100kwh之间（并网、离网系统均符合资格）
- 并网电池需具备接入虚拟电厂（VPP）能力
- 仅前 50 kwh 容量可享受补贴
- 电池系统不得曾获其他补贴
- 电池和逆变器须列于清洁能源委员会（CEC）批准的产品清单 [清单在此处](https://cleanenergycouncil.org.au/industry-programs/products-program/batteries)
- 必须由SAA（Standards Australia Accreditation）认证的安装工人进行安装 [可在此输入安装工姓名查找](https://saaustralia.com.au/accreditation-status-check/)
- 电动汽车（EV）电池不适用本补贴
- 多模块/可堆叠电池视为单一电池单元
   - e.g. 比亚迪（BYD）和阳光电源（SunGrow）的堆叠电池系统，只要同时安装就会被视为一个储能系统。如，两个9.6kwh的阳光电源电池模块可以通过并联安装组合成一个19.2千瓦时的系统，此时补贴将适用于以19.2kwh计

**补贴的计算方式，以安装电池为例：**

通常情况下，STCs的交易价格约为40澳元（[此价格存在波动](https://solarcalculator.com.au/battery-storage/rebate/)）。扣除行政费用后，实际价值约为37澳元。


| 年份   | 安装每kwh电能获得的STCs | 每kwh计算              | 45kwh     | 50kwh(上限) | 55kwh     |
| ---- | --------------- | ------------------- | --------- | --------- | --------- |
| 2025 | 9.3             | 9.3 \* 37 ≈ 344 AUD | 15,480AUD | 17,200AUD | 17,200AUD |
| 2026 | 8.4             | 310.8 AUD           | 13,968AUD | 15,540AUD | 15,540AUD |
| 2027 | 7.4             | ...                 | ...       | ...       | ...       |
| 2028 | 6.5             |                     |           |           |           |
| 2029 | 5.6             |                     |           |           |           |
| 2030 | 4.7             |                     |           |           |           |

2025年，一个10度电的电池大约能得到3,440澳元的补贴。补贴的上限是50度电。

[STC计算器]([REC Registry - 小型发电机组 STC 计算器](https://www.rec-registry.gov.au/rec-registry/app/calculators/sgu-stc-calculator))
[补贴计算器]([STC 计算器 |计算您的太阳能回扣](https://solarcalculator.com.au/stc-calculator/))

#### 1.1.2 太阳能板补贴（PV）

[申请步骤](https://cer.gov.au/schemes/renewable-energy-target/small-scale-renewable-energy-scheme/small-scale-renewable-energy-systems/rooftop-solar#installing-rooftop-solar)

**申请条件**：

- 系统功率必须低于100kW
- 由 SAA 认可的安装人员来设计和安装
- 太阳能板被清洁能源委员会 (CEC)批准[产品清单](https://cleanenergycouncil.org.au/industry-programs/products-program/modules "已批准模块列表")
- 逆变器被 CEC 认可[逆变器列表](https://cleanenergycouncil.org.au/industry-programs/products-program/inverters "已批准的逆变器列表")
- 安装之日起 12 个月内申请 STC
- 系统必须符合澳大利亚和新西兰、所有地方、州和联邦的要求

#### 1.1.3 太阳能热水器 Solar Water Heater

与PV的区别是，太阳能热水器系统直接用太阳能通过集热器加热水。因为它们产生热量而不是电能。

**申请条件**：

- 系统容量: 小于 700 L，容量超过 700 升的型号必须提供额外的文件才有资格获得STC
- 型号在[官方名单](https://cer.gov.au/schemes/renewable-energy-target/small-scale-renewable-energy-scheme/small-scale-renewable-energy-systems/solar-water-heaters/register-solar-water-heaters))上

 [申请步骤](https://cer.gov.au/node/3678#installing-a-water-heater-system).
#### 1.1.4 空气源热泵 Air Source Heat Pump

空气源热泵从空气中提取热量并将其泵入储水箱。该系统包括一个热泵单元（如分体式空调的室外机）和一个储罐。该装置由您的普通家用电线或太阳能电池板供电。

**申请条件**： 

- 系统容量: 小于 425 升
- 型号在[官方名单](https://cer.gov.au/schemes/renewable-energy-target/small-scale-renewable-energy-scheme/small-scale-renewable-energy-systems/solar-water-heaters/register-solar-water-heaters))上

[申请步骤](https://cer.gov.au/schemes/renewable-energy-target/small-scale-renewable-energy-scheme/small-scale-renewable-energy-systems/solar-water-heaters-and-air-source-heat-pumps#installing-a-water-heater-system "Solar water heaters and air source heat pumps").

#### 1.1.5 风力涡轮机 Wind Turbine

典型的风力涡轮机系统由涡轮机、塔架、控制器、并网逆变器和仪表组成。风使涡轮机的螺旋桨叶片绕着转子转动，转子使发电机旋转并产生电力。电力储存在离网风力涡轮机的电池中，或输出到并网风力涡轮机的电网中。

申请条件：

- 系统容量：小于 10 kW.
- 年发电量：小于 25 MWh.

[申请步骤](https://cer.gov.au/schemes/renewable-energy-target/small-scale-renewable-energy-scheme/small-scale-renewable-energy-systems/small-scale-wind-and-hydro-systems "Small-scale wind and hydro systems").

#### 1.1.6 水利系统 Hydro System

典型的小型水力发电系统由管道、涡轮机、发电机和并网逆变器组成。管道将水引导到涡轮机，涡轮机将流动的水转化为旋转能。发电机将旋转能转化为电能。电力储存在离网水电系统的电池中，或输出到并网水电系统的电网中。

申请条件：

- 系统容量：小于 6.4 kW.
- 年发电量：小于 25 MWh.

[申请步骤](https://cer.gov.au/schemes/renewable-energy-target/small-scale-renewable-energy-scheme/small-scale-renewable-energy-systems/small-scale-wind-and-hydro-systems "Small-scale wind and hydro systems").




### 1.2 适用澳大利亚全境的LRET计划（大系统）


**大规模可再生能源目标 Large-scale Renewable Energy Target (LRET)**  ，是[澳大利亚可再生能源目标 （RET）](https://cer.gov.au/schemes/renewable-energy-target) 计划的一部分，可以获得**商业太阳能回扣**。通过 LRET，符合条件的**企业**可以获得太阳能生产的持续经济利益，帮助澳大利亚减少碳足迹并实现能源目标。

 LRET 的目标：每年产生 33,000 吉瓦时的可再生能源。

**补贴形式**：大规模发电证书，Large-scale Generation Certificates (LGCs)。

企业每产生一兆瓦时 （MWh） 的可再生电力，就可以获得 1 个 LGC。LGC可以在市场上出售给公用事业公司和其他需要实现可再生能源目标的公司。目前每个LGC的价格约为 46.25 美元（价格有所波动）。

系统产生的电力越多，获得的LGC就越多，收入就越多。

**申请条件**：

- 商业和公用事业规模的安装，如大型太阳能发电场
- 系统容量必须超过 100kW
- 获得得清洁能源监管机构的认可



### 1.3 太阳能上网电价 Feed-in Tariff, FiT

太阳能上网电价（Feed-in Tariff, FiT）​​ 是电力公司对用户回馈至电网的每度太阳能电力所支付的经济补偿，有时也被称为 ​回购电价（buy-back rate）​或 ​太阳能奖励计划（solar bonus scheme）。

当太阳能电池板发电时，电力会优先直接供给家用电器使用，多余的电能要么储存在电池中，要么输送回电网。每向电网输送1千瓦时（kWh）的多余电能，电力公司会向用户支付费用，以抵扣电费的形式来支付。

FiT无需特别申请。**上网电价费率因 州 和 零售商 而异**。[点击查询](https://solarcalculator.com.au/feed-in-tariffs/)


如


| 地区   | 返利金额                  | 备注                          |
| ---- | --------------------- | --------------------------- |
| 维多利亚 | 电费从每kwh 3.3美分降至0.04美分 | 一旦并网系统安装并运行，就可以开始获得太阳能上网电价。 |


![renewable-energy-1.jpg (800×533)](https://cdn-ecjlk.nitrocdn.com/fysFpaNSVfBhfzYkFaKIFqNprQBwyKad/assets/images/optimized/rev-81942de/solaremporium.com.au/wp-content/uploads/2024/05/renewable-energy-1.jpg)
### 1.4 澳大利亚各州/省的补贴
#### 1.4.1 维多利亚 VIC

**适用SRES的太阳能板补贴、电池补贴。适用上网电价**

维多利亚州，即墨尔本所在地。**维多利亚是激励措施最慷慨的一个州。维多利亚只有 29% 的家庭拥有太阳能，而全澳平均水平为 38%。维多利亚州政府设定了到 2030 年实现 65% 的可再生能源目标，目前该州只有 40% 的电力由可再生能源提供。[来源](https://cer.gov.au/markets/reports-and-data/small-scale-installation-postcode-data)**


##### 维州太阳能板补贴 Victorian solar panel rebate

当前补贴稳定在1400 AUD，维州尚未确定何时结束补贴。

**申请条件**：
- 拥有并居住在此太阳能板的安装地址
- 家庭应税收入合计每年低于 210,000 美元
- 房屋价值低于 300 万美元（如在建，则房屋的竣工价值低于 300 万美元）
- 您前没有收到过 VIC 太阳能住宅计划下的回扣
- 在过去 10 年内没有在该物业安装太阳能电池板
- 电池板、逆变器和/或电池必须出现在 Solar Victoria 批准的产品[清单](https://www.solar.vic.gov.au/product-lists)上
- 必须由 Solar Victoria 授权零售商、CEC认证的安装商来安装太阳能板系统
- 安装商持有“A 级”电气执照
- 商家提供至少 5 年的整个系统保修

##### 房产租赁太阳能补贴 Victorian solar rebate for rental providers

用户将房产出租给租户，则可以在出租物业上安装太阳能电池板时，申请维州太阳能补贴。金额为 1,400 AUD。您必须满足与 维州太阳能板补贴 相同的资格要求，以及如下附加标准：

- 租客的总收入必须低于 1,400 美元
- 该房产价值不到 300 万美元
##### Solar Victoria 无息贷款

州政府提供为符合条件的维多利亚州居民提供购买新太阳能电池板 1,400 美元的免息贷款，分4年支付。

#### 1.4.2 新南威尔士NSW

新南威尔士即悉尼所在地

**适用SRES的太阳能板补贴、电池补贴。适用上网电价**

此外还有进一步的：

##### VPP补贴

 2025 年 7 月 1 日起，将自用的储能系统并入虚拟电网，可获最高达1,500 AUS的补贴。适用于所有将电池连接到 VPP 的家庭和企业。可以叠加澳洲联邦政府的电池补贴。

条件
- 必须是新南威尔士州居民（不设收入门槛）
-  将已安装或新安装的电池并入虚拟电网
- 电池的保修期必须至少剩余 6 年
- 电池在 2 kWh 到 28 kWh 之间
- 经认可的供应商/安装商

新南威尔士州 VPP 回扣的确切值因电池大小和 VPP 提供商而异。通常，属于以下范围：
- 400 kWh 电池的价格在 550 美元至 10 美元之间
- 1,000 kWh 电池在 1,500 美元至 27 美元之间

##### 家庭节能升级 Household energy saving upgrades

可用的补助金包括：

- 照明升级：用LED筒灯代替卤素筒灯。
- 空调升级：改用更节能的空调系统。
- 热水系统升级：升级到更节能的热水系统。
- 泳池泵升级：用更节能的型号更换泳池泵。

每项的金额根据设备的大小而有所不同。还必须满足一些资格要求才能获得回扣。[详情界面](https://www.energy.nsw.gov.au/households/rebates-grants-and-schemes/household-energy-saving-upgrades)。
##### 低收入电费回扣 Low-income electricity bill rebate

新南威尔士州的低收入家庭可获得每年最高 350 澳元的电费回扣

**申请条件**：

- 住在新南威尔士州与电网相连的房产上
- 名下有一个电力账户
- 持有符合回扣条件的优惠卡, e.g. 医疗卡，低收入健康卡，养老金领取者优惠卡，退伍军人事务部 （DVA） 金卡

[详情界面](https://www.service.nsw.gov.au/transaction/apply-for-the-low-income-household-rebate-retail-customers)

##### 地方政府回扣 Local NSW government rebates

[兰德威克市议会](https://www.randwick.nsw.gov.au/business/business-resources/sustainability-rebates "Randwick City Council")可持续发展回扣，Randwick City Council sustainability rebates

- 太阳能电池板 – 10% 回扣，最高可达 500 美元
- 太阳能电池 – 10% 回扣高达 1,000 美元
- 太阳能健康检查 – 50% 回赠高达 100 美元



#### 1.4.3 南澳大利亚州 SA

**适用SRES的太阳能板补贴、电池补贴。适用上网电价**
##### 太阳能板补贴

**申请条件**：
- 系统由 SAA 安装人员设计和安装
- 面板和逆变器在 CEC 的清单中
- 系统小于 100kW

平均尺寸为 6.6kW 的太阳能板可获得约 2,160 美元的补贴。

##### 电费补贴

所有南澳家庭有每年 150 澳元的电费补贴。

##### 阿德莱德市 Adelaide

阿德莱德的房主和企业还可以享受当地太阳能光伏激励措施。

**阿德莱德的房主**

阿德莱德市为特许卡持有者、租户和分层管理的住宅物业提供[阿德莱德新安装太阳能电池板](https://solarcalculator.com.au/solar-panels/adelaide/ "new solar panel installations in Adelaide")的20% 的折扣。不同系统大小节省的费用如下：
- 20% 最高 1,000 美元（1.5kW - 10kW 系统）
- 20% 最高 2,500 美元（10kW - 20kW 系统）
- 20% 高达 5,000 美元（20kW+ 系统）


**阿德莱德的企业**

安装太阳能电池板的企业可获得小额回扣：

- 20% 最高 1,000 美元（10kW 至 20kW 系统）
- 20% 高达 2,000 美元（20+kW 系统）

安装新电池的阿德莱德企业可获得高达 50% 的电池补贴（最高 1,000 AUS）


#### 1.4.4 西澳大利亚 WA

**适用SRES的太阳能板补贴、电池补贴。适用上网电价**


##### 西澳住宅计划 WA Residential Battery Scheme

西澳补贴适用于前 10 kWh 容量的电池。但具体回扣的金额因电力分销商而异。

如Synergy 客户最多可获得 1,300 AUS的新电池折扣，而 Horizon 客户最多可获得 3,800 AUD。

##### 无息贷款 WA 


西澳为符合条件的居民提供价值高达 10,000 美元的无息贷款。偿还期限为 10 年。

只有总收入低于 210,000 美元的家庭才能获得贷款。

#### 1.4.5 塔斯马尼亚 TAS

**适用SRES的太阳能板补贴、电池补贴。适用上网电价。**

塔斯马尼亚居民可以获得高达 10,000 美元的无息贷款，帮助他们购买电池系统,进行一系列节能投资。偿还期限在一到三年。

#### 1.4.6 首都领地 ACT (Australian Capital Territory)

**适用SRES的太阳能板补贴、电池补贴。适用上网电价。**

根据[可持续家庭计划](https://solarcalculator.com.au/blog/act-sustainable-household-scheme/ "Sustainable Household Scheme")，澳大利亚首都特区的房主可以获得高达 15,000 美元的低息贷款，以帮助进行一系列节能投资，包括家庭太阳能电池存储。贷款可以在 10 年内还清。

