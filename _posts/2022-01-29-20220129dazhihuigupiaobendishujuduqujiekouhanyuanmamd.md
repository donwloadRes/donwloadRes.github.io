---
layout: post
title: "大智慧股票本地数据读取接口（含源码）"
date:   2021-09-05
tags: [num,FxjData2FinData,dm,char,rq]
comments: true
author: admin
---
# 大智慧股票本地数据读取接口（含源码）

## 描述

本资源文件适用于“大智慧新一代 Level-2 V3.03.08.0801”的版本，提供了详细的本地数据读取接口及源码。附件中包含了数据表结构，方便用户理解和使用。

## 数据表结构

### 代码数据 (cndm)
- **dm**: 代码 (char)
- **jc**: 简称 (char)

### 行情数据 (cnfqhq)
- **dm**: 代码 (char)
- **rq**: 日期 (date)
- **kp**: 开盘 (num)
- **zg**: 最高 (num)
- **zd**: 最低 (num)
- **sp**: 收盘 (num)
- **sl**: 成交数量 (num)
- **je**: 成交金额 (num)
- **yz**: 复权因子 (num)

### 除权数据 (cncq)
- **dm**: 代码 (char)
- **rq**: 日期 (date)
- **fh**: 分红 (num)
- **sgbl**: 送股比例 (num)
- **pgbl**: 配股比例 (num)
- **pgjg**: 配股价格 (num)

### 股本数据 (cngb)
- **dm**: 代码 (char)
- **rq**: 日期 (date)
- **zgb**: 总股本 (num)
- **ltg**: 流通A股 (num)
- **bg**: B股 (num)
- **hg**: H股 (num)

### 财务指标 (cncw)
- **dm**: 代码 (char)
- **rq**: 日期 (date)
- **eps**: 每股收益(全面摊薄) (num)
- **eps1**: 每股收益(加权平均) (num)
- **naps**: 每股净资产 (num)
- **roe**: 净资产收益率(全面摊薄) (num)
- **roe1**: 净资产收益率(加权平均) (num)

### 财务报表 (cncwbb)
- **dm**: 代码 (char)
- **rq**: 日期 (date)
- **bsdqtzje**: 短期投资净额 (num)
- **bsyszkje**: 应收帐款净额 (num)
- **bschje**: 存货净额 (num)
- **bsldzc**: 流动资产 (num)
- **bscqtzje**: 长期投资净额 (num)
- **bsgdzc**: 固定资产 (num)
- **bswxzc**: 无形及其他资产 (num)
- **bszzc**: 总资产 (num)
- **bsdqjk**: 短期借款 (num)
- **bsyfzk**: 应付帐款 (num)
- **bsldfz**: 流动负债 (num)
- **bscqfz**: 长期负债 (num)
- **bsfz**: 负债合计 (num)
- **bsgb**: 股本 (num)
- **bsssgdqy**: 少数股东权益 (num)
- **bsgdqy**: 股东权益 (num)
- **bszbgj**: 资本公积 (num)
- **bsyygj**: 盈余公积 (num)
- **iszysr**: 主营业务收入净额 (num)
- **iszycb**: 主营业务成本 (num)
- **iszylr**: 主营业务利润 (num)
- **isqtlr**: 其它业务利润 (num)
- **isyyfy**: 营业费用 (num)
- **isglfy**: 管理费用 (num)
- **iscwfy**: 财务费用 (num)
- **istzsy**: 投资收益 (num)
- **islrze**: 利润总额 (num)
- **issds**: 所得税 (num)
- **isjlr**: 净利润 (num)
- **iskchjlr**: 扣除经常性损益后的净利润 (num)
- **iswfplr**: 未分配利润 (num)
- **cfjyhdxjlr**: 经营活动现金流入 (num)
- **cfjyhdxjlc**: 经营活动现金流出 (num)
- **cfjyhdxjje**: 经营活动现金净额 (num)
- **cftzxjlr**: 投资现金流入 (num)
- **cftzxjlc**: 投资现金流出 (num)
- **cftzxjje**: 投资现金净额 (num)
- **cfczxjlr**: 筹措现金流入 (num)
- **cfczxjlc**: 筹措现金流出 (num)
- **cfczxjje**: 筹措现金净额 (num)
- **cfxjjze**: 现金及现金等价物净增额 (num)
- **cfxsspxj**: 销售商品收到的现金 (num)
- **mgsy**: 每股收益 (num)
- **mgjzc**: 每股净资产 (num)
- **tzmgjzc**: 调整后每股净资产 (num)
- **mgzbgjj**: 每股资本公积金 (num)
- **mgwfplr**: 每股未分配利润 (num)
- **mgjyxjllje**: 每股经营活动产生的现金流量净额 (num)
- **mgxjzjje**: 每股现金及现金等价物增加净额 (num)
- **mll**: 毛利率 (num)
- **zyywlrl**: 主营业务利润率 (num)
- **jll**: 净利率 (num)
- **zzcbcl**: 总资产报酬率 (num)
- **jzcsyl**: 净资产收益率 (num)
- **xsxjzb**: 销售商品收到的现金占主营收入比例 (num)
- **yszczzl**: 应收帐款周转率 (num)
- **chzzl**: 存货周转率 (num)
- **gdzczzl**: 固定资产周转率 (num)
- **zyywzzl**: 主营业务增长率 (num)
- **jlrzzl**: 净利润增长率 (num)
- **zzczzl**: 总资产增长率 (num)
- **jzczzl**: 净资产增长率 (num)
- **ldbl**: 流动比率 (num)
- **sdbl**: 速动比率 (num)
- **zcfzbl**: 资产负债比率 (num)
- **fzbl**: 负债比率 (num)
- **gdqybl**: 股东权益比率 (num)
- **gdzcbl**: 固定资产比率 (num)
- **kchmgjlr**: 扣除经常性损益后每股净利润 (num)

### 交易日期 (cnrq)
- **rq**: 交易日期 (date)

### 板块数据 (cnbk)
- **lb**: 类别 (char)
- **bk**: 板块 (char)
- **dm**: 代码 (char)
- **zz**: 创建者 (char)

### 存款利率 (cnll)
- **dm**: 代码 (char)
- **jc**: 简称 (char)
- **rq**: 变动日期 (date)
- **ll**: 利率 (num)

### 港股代码 (hkdm)
- **dm**: 代码 (char)
- **jc**: 简称 (char)

### 港股行情 (hkhq)
- **dm**: 代码 (char)
- **rq**: 日期 (date)
- **kp**: 开盘 (num)
- **zg**: 最高 (num)
- **zd**: 最低 (num)
- **sp**: 收盘 (num)
- **sl**: 成交数量 (num)
- **je**: 成交金额 (num)

## 使用说明

1. **调用格式**: `FxjData2FinData(MarketDataTypeFinDataLib)`
   - **Market**: 市场代码（SH为沪市，SZ为深市，BK为板块指数，HK等其他市场代码）
   - **DataType**: 数据类型（如dm、cq、cw0、hq0等，具体含义见注释）
   - **FinDataLib**: 目标逻辑库（若目标逻辑库不存在，则设为Work）

2. **数据文件占用处理**: 如果数据文件已被分析家等软件占用导致无法打开，程序将自动复制一份该文件并从备份文件中读取数据。

3. **数据补充**: 程序将自动补充数据，即如果目标表不存在则建立并添加数据，如果目标表已存在则判断表中每只证券的最新数据，然后只添加数据表中所缺少的数据。

## 参数设置

```sas
%let FxjPath=C:\fxj\; /* 分析家安装目录 */
%let HqmbFilesToRead=2; /* 分笔成交读取文件数，若为1则只读取report.dat，若为值n则除了读取Report.dat外还将读取(n-1)个最新.PRP历史分笔成交数据文件 */
```

## 数据转换示例

```sas
/* 沪市 */
%FxjData2FinData(shdmFinData); /* dm--证券代码，原数据集将保存为xxDM_bak */
%FxjData2FinData(shcqFinData); /* cq--除权数据 */
%FxjData2FinData(shcw0FinData); /* cw0--最新财务数据 */
%FxjData2FinData(shhq0FinData); /* hq0--最新行情 */
%FxjData2FinData(shhqFinData); /* hq--每日行情 */
%FxjData2FinData(shhqmbFinData); /* hqmb--每笔成交 */
%FxjData2FinData(shhq5FinData); /* hq5--5分钟行情 */
%FxjData2FinData(shfpFinData); /* fp--分红送配(专业财务数据) */
%FxjData2FinData(shgbFinData); /* gb--股本结构(专业财务数据) */
%FxjData2FinData(shcwFinData); /* cw--财务数据(专业财务数据) */
%FxjData2FinData(shgdFinData); /* gd--十大股东(专业财务数据) */
%FxjData2FinData(shjjjzFinData); /* jjjz--基金净值(专业财务数据) */
%FxjData2FinData(shjjzhFinData); /* jjzh--基金投资组合(专业财务数据) */

/* 深市 */
%FxjData2FinData(szdmFinData);
%FxjData2FinData(szcqFinData);
%FxjData2FinData(szcw0FinData);
%FxjData2FinData(szhq0FinData);
%FxjData2FinData(szhqFinData);
%FxjData2FinData(szhqmbFinData);
%FxjData2FinData(szhq5FinData);
%FxjData2FinData(szfpFinData);
%FxjData2FinData(szgbFinData);
%FxjData2FinData(szcwFinData);
%FxjData2FinData(szgdFinData);
%FxjData2FinData(szjjjzFinData);
%FxjData2FinData(szjjzhFinData);

/* 板块及板块指数 */
%FxjData2FinData(bkzhFinData); /* 板块数据: Market=bk, DataType=zh... */
%FxjData2FinData(bkdmFinData);
%FxjData2FinData(bkhq0FinData);
%FxjData2FinData(bkhqFinData);
%FxjData2FinData(bkhqmbFinData);
%FxjData2FinData(bkhq5FinData);

/* 香港市场 */
%*FxjData2FinData(hkdmFinData);
%*FxjData2FinData(hkhq0FinData);
%*FxjData2FinData(hkhqFinData);
%*FxjData2FinData(hkhqmbFinData);
%*FxjData2FinData(hkhq5FinData);
```

## 数据格式说明

### 日线数据文件 (day.dat)
- **文件标志**: int
- **未知**: int
- **保留**: int
- **证券总数**: int
- **未知**: int
- **未知**: int
- **未知**: int
- **证券代码**: byte[10]
- **日线记录数**: int
- **记录块号**: char[25]

### 1分钟数据文件 (min1.dat)
- **文件名**: MIN1.DAT
- **起始地址**: 0x41000
- **块大小**: 16384
- **记录大小**: 32
- **字段**: dm代码, rq日期, kp开盘, zg最高, zd最低, sp收盘, sl成交数量, je成交金额

### 5分钟数据文件 (min.dat)
- **文件名**: MIN.DAT
- **起始地址**: 0x41000
- **块大小**: 8192
- **记录大小**: 32
- **字段**: dm代码, rq日期, kp开盘, zg最高, zd最低, sp收盘, sl成交数量, je成交金额

### 最新行情 (STKINFO60.dat)
- **文件名**: STKINFO60.DAT
- **起始地址**: 0x68A8A6
- **块大小**: 0
- **记录大小**: 273
- **字段**: dm代码, jc简称, rq更新时间, zs昨收, kp今开, zg最高, zd最低, sp最新, sl总手数, je金额, xss现手数, ztj涨停价, dtj跌停价, np内盘, wp外盘, mrjg1买一价, mrsl1买一量, mrjg2买二价, mrsl2买二量, mrjg3买三价, mrsl3买三量, mrjg4买四价, mrsl4买四量, mrjg5买五价, mrsl5买五量, mcjg1卖一价, mcsl1卖一量, mcjg2卖二价, mcsl2卖二量, mcjg3卖三价, mcsl3卖三量, mcjg4卖四价, mcsl4卖四量, mcjg5卖五价, mcsl5卖五量

### 分笔成交数据文件 (report.dat)
- **文件名**: REPORT.DAT
- **起始地址**: 0x41000
- **块大小**: 12272
- **记录大小**: 52
- **字段**: dm代码, rq日期, zjcj最近成交价, zss总手数, je金额, xss现手数, mm内外盘, mr1jg买一价, mr1sl买一量, mr2jg买二价, mr2sl买二量, mr3jg买三价, mr3sl买三量, mr4jg买四价, mr4sl买四量, mr5jg买五价, mr5sl买五量, mc1jg卖一价, mc1sl卖一量, mc2jg卖二价, mc2sl卖二量, mc3jg卖三价, mc3sl卖三量, mc4jg卖四价, mc4sl卖四量, mc5jg卖五价, mc5sl卖五量, bs总笔数

### 财务数据 (STKINFO60.dat)
- **文件名**: STKINFO60.DAT
- **起始地址**: 0x4c2a
- **块大小**: 2227
- **记录大小**: 273
- **字段**: dm代码, rq报告期, gxrq更新日期, ssrq上市日期, col1每股收益, col2每股净资产, col3净资产收益率, col4每股经营现金, col5每股公积金, col6每股未分配, col7股东权益比, col8净利润同比, col9主营收入同比, col10销售毛利率, col11调整每股净资产, col12总资产, col13流动资产, col14固定资产, col15无形资产, col16流动负债, col17长期负债, col18总负债, col19股东权益, col20资本公积金, col21经营现金流量, col22投资现金流量, col23筹资现金流量, col24现金增加额, col25主营收入, col26主营利润, col27营业利润, col28投资收益, col29营业外收支, col30利润总额, col31净利润, col32未分配利润, col33总股本, col34无限

## 下载链接

[大智慧股票本地数据读取接口含源码](https://pan.quark.cn/s/3faee9b1c708)