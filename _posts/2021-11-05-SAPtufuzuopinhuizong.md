---
layout: post
title: "SAP屠夫作品汇总"
date:   2021-09-23
tags: [Define,Tcode,物料,SAP,Planning]
comments: true
author: admin
---
# SAP屠夫作品汇总

## 描述

本资源文件汇总了SAP屠夫在SAP系统配置、财务会计、控制、资产管理、应收应付、特别总账、合并会计、投资管理、现金管理、内部订单、成本中心会计、成本核算单、生产成本控制、利润分析、物料管理、生产计划、销售与分销、基础配置、ABAP开发、BW数据仓库、战略企业管理等方面的作品和配置实例。内容涵盖了从基础设置到高级配置的各个方面，适合SAP顾问、开发人员以及对SAP系统有深入了解需求的用户参考和学习。

## 目录

### 1. General Settings
- 检查度量单位(Check Units of Measurement)

### 2. Financial Accounting
- Financial Accounting Global Settings
  - 例1：功能范围的应用
  - 例2：业务范围(Business Area)
  - 年度变式(Fiscal Year)
  - 会计凭证(Document)：如何限制不同财务用户使用不同的财务凭证类型
  - Field status和Coding block subscreen
  - Validation凭证的确认
  - Substitution凭证的退代
  - 几个相关函数FI_VALIDATION_DOC|FI_VALIDATION_HEADER
  - 货币类型和外币评估
  - ERP货币类型和外币业务
  - 汇率与外币评估
  - 财务分类帐

### 3. Tax on Purchase & Sales
- 大话MM定价增值税处理
- SAP 税务配置
- SD篇 tax
- SD一周通系列
- SD定价实例
- 收入科目确定
- 税务设置

### 4. Special Purpose Ledger
- 基本设置(Basic Settings)
  - Perform Preparation
  - Maintain Coding Block
  - Tables
  - Maintain Table Directory
  - Maintain Fixed Field Movements
  - Master Data
  - Production Start-Up Preparation
  - Validation
  - Substitution
  - User Exits
- 计划(Planning)
- 实际过帐(Actual Posting)
- 期间处理(Periodic Processing)
- 信息系统(Information System)
- 工具(Tools)
  - 例1：使用SPL出中方会计报表
  - 例2：维护coding block screen

### 5. EC-CS Consolidation
- 合并会计处理方法
- 第14夜：合并数据建模
  - 建立合并源数据基础信息立方体(Tcode:RSA1)
  - 建立合并数据基础信息立方体(Tcode:RSA1)
  - BCS建模(Tcode:UCWBUCWB01UCMP0)
  - 设置合并范围
  - 设置合并参数(Tcode:UCMP0)
  - 设置合并源数据基础
  - 合并会计科目表和合并频率设置
  - BCS60数据增强的功能
  - 例1：使用混合合并单元
  - 例2：BCS和ECCS等合并系统简单对比
- 第五节：子分配和细分类别

### 6. SAP会计科目自动分配配置大全
- Maintain Accounting Configuration(概览)
- Automatic Posting Configuration (MM Module)
  - 例1：如何使用Valuation group code
  - 例2：PO condition和OBYC
  - 例3：使用PO处理委外加工
  - 例4：Account assignment的逻辑分析
  - 例5：采购运费处理
  - 例6：P&L科目和成本要素的建立
  - 例7：采购科目分配设置
  - 例8：汇率变更影响发票校验
  - 例9：月结GR/IR处理
  - 戏说一下SAP的清帐
  - Vendor的AP和Customer的AR能被对清需要在Vendor和customer主数据设置一下

### 7. Asset Accounting
- 折旧方法和折旧码
- 使用Substitution退还固定资产折旧某资产折旧的费用科目和折旧金额
- FB08如何reverse多余的折旧凭证

### 8. 应收应付(Accounts Receivable and Accounts Payable)配置
- Report painter外资公司如何出中方式报表
- FICO统驭和中间清算
- Field status and Coding block subscreen 字段状态组实例
- 特别总帐标识
- 预付款处理
- 发票冻结(Invoice Block)
- Dunning AR催款配置
- 浅谈表结法和帐结法
- Company和Company Code的区别

### 9. Investment Management
- 投资管理
- 投资计量
- 投资订单预算

### 10. Treasury
- 现金管理和预算控制
- 第一节：现金管理配置
- 第二节：现金管理业务操作
- 现金管理一日通

### 11. CO - Controlling
- Internal Order 内部订单
  - 订单主数据
  - 订单审批
  - 订单计划
  - 内部订单预算
  - 结算规则自动生成
  - 内部订单(Internal Orders) 审批流程配置
- CO-CCA Cost Center Accounting
  - 分配分摊
  - 最牛B最灵活的分配分摊依据--统计指标
  - 作业类型
  - 建立type 43次级成本要素(Tcode:KA06)
  - 建立作业类型(Tcode:KL01)
  - 建立生产成本中心(Tcode:KS02)
  - 成本中心作业量计划(Tcode:KP26|KP27)
  - 建立成本中心费用计划(Tcode:KP06|KP16/KP17/KP36/KP37)
  - 计算计划价格(Tcode:KSPI)
  - 维护分割结构(Tcode:OKES/OKEW)
  - 建立工作中心
  - 建立统计指标
  - 重过帐和直接作业分摊
  - 分配分摊
- CO-PC
  - Costing Sheet 成本核算单
  - Define Origin Groups(Tcode:OKZ1)
  - Maintain Overhead Cost Elements（Tcode：KA06）
  - Define Costing sheets
  - Define Calculation Bases
  - Define Percentage Overhead Rates（Tcode:S_ALR_87008275）
  - Define Quantity_Based Overhead Rates
  - Define Credits
  - Develop Enhancement
  - Define Overhead Key
  - Define Overhead Group
  - Define Cost Component Structure（Tcode：OKTZ）
  - Error Management
  - 使用成本核算单的标准成本估算实例
  - 标准成本Cost variant的Valuation Variant 001(Tcode:OKK4)
  - 作业计划价格和Routing检查(CA03)
  - 作业计划价格检查(KP26)
  - 成本核算单和成本组件结构
  - 例1：Origin group的使用
  - 例2：Costing sheet结构和成本估算实例
  - 例3
  - 例4：ZROY Calculation Base增强
  - 例5：细说Cost component Structure和Cost Variant关系
- 生产成本控制(Product Cost Controlling)后台配置
  - Product Cost Planning
  - Basic Settings for Material Costing
  - Plan Target Actual and Control Cost
  - Define Cost-Accounting-Relevant Default Values
  - Error message 管理
  - Work in Process
  - Variance Calculation
  - Settlement
  - Future costing 方案(技术篇)
  - 业务背景
  - 业务未定部分
  - 解决方案
  - CO-PC部分
  - CO-PA部分
  - 需要确定因素
  - CK11N取info record 分析报告
  - Purchase Info record tables
  - 取什么info record
  - Cost Estimation 成本估算
  - 成本估算变式
  - Define Costing Types
  - Define Valuation Variants
  - Material valuation
  - Actity Type/Process
  - Subcontracting
  - External Processing
  - Overhead
  - Price Factors
  - Define Date Control
  - Define Quantity Structure Control
  - Define Transfer Strategy
  - Define Reference Variants
  - Define Costing Variants
  - 标准成本估算
  - 例1：Last PO Price Cost Estimate
  - 例2：Future Costing for COPA
  - 例3
  - 数量结果控制设置
  - 重复制造生产配置
  - 按库存生产配置(Make-to-Stock)
  - 按订单生产配置(Make-to-order)
- CO-PA
  - 利润分析(Profitability Analysis)后台配置
  - Structures
  - Maintain Characteristics
  - Maintain Value Fields
  - Maintain Operating Concern
  - Sample Operating Concerns
  - Define profitability Segment Char.
  - Set Operating Concern
  - Master Data
  - Maintain Characteristic Values
  - Define Characteristics Hierarchy
  - Define Characteristic Derivation
  - Valuation Strategies
  - Set Up Valuation Using Material Cost Estimate
  - Set Up Conditions and Costing Sheets
  - Planning
  - Initial Steps
  - Define Number Ranges for Planning Data
  - Maintain Versions
  - Assign Quantity Fields
  - Planning Framework
  - Set Up Planning Framework
  - Create Planning Level fro Planning Layout
  - Display Planner Profiles
  - Manual Entry of Planning Data
  - Define Planning layout
  - Define Value Field Assignments
  - Define Distribution Profiles
  - Calculated Values as Reference
  - Integrated Planning
  - Planning Aids
  - Reorganization
  - Flows of Actual Values
  - Initial Steps
  - Define Number Ranges for Actual Postings
  - Maintain Characteristic Groups
  - Assign Cha. Grp. for Assignment Screen
  - Assing Char. Grp. For Line Item Screen
  - Maintain Value Field Groups
  - Summarize Data During Update
  - Store Quantities In CO-PA Std. Unit of Measure
  - Transfer of Incoming Sales Orders
  - Transfer of Billing Documents
  - Order and Project Settlement
  - Direct Posting from FI/MM
  - Settlement of Production Variances
  - Transfer of Overhead
  - Transfer Customer Rebate Agreements
  - Multiple Valuation Approaches/Transfer Price
  - Periodic Adjustments
  - Activate Profitability Analysis
  - 定义经营范围
  - 获利分析段PSG
  - 特征值派生和值字段评估
  - 基本设置(Basic Settings)
  - 企业组织(Enterprise Organization)
  - 主数据(Master Data)
  - 利润中心分配(Assignments to Profit Centers)
- SAP屠宰行业CO解决方案
  - 业务背景
  - SAP实现
  - 建立物料
  - 建立BOM
  - 外包给屠夫宰
  - 使用外包工序
  - 关于联产品工单成本怎么结算
  - 工单
- Material Ledger 物料分类账详解
  - ML功能简介
  - 标准价Pk加权平均价
  - 差异来源和差异处理
  - SAP差异科目设置
- 利润中心(Profit Center Accounting)
  - 基本设置(Basic Settings)
  - 企业组织(Enterprise Organization)
  - 主数据(Master Data)
  - 利润中心分配(Assignments to Profit Centers)
  - 转移价格(Transfer Prices)

### 12. Logistics - General
- 销售运作计划(SOP)和利润计划
- LIS配置
  - 应用Sales Flexible Planning
  - 使用PA Planning Framework(KEPM)
  - PA Valuation Stratege

### 13. MM Material Management
- PO Account Assignment 增强 Coding Block
- Background
- Related IMG
- Step 1：Define valuation class for those non-material
- Step 2：Define PO Account Assignment Categories
- Step 3：Assign account to VBR
- Step 4：Where we define valuation class
- Q&A
  - How to Activate Direct Posting to G/L Accounts and Material Account
  - What will Happen?
  - Mark delv. Completed
- 物料移动类型和后勤自动科目设置
- 分割评估和混合成本
  - 业务背景
  - 配置分割评估
  - 建立物料主数据
  - 建立cosing mix ratio (Tcode:CK91/CK91N|CK94)
  - Valuation variant分析
- 后勤一般设置(Logsticis-General)
- 物料主数据(Material Master)
- MM Condition配置
- PO审批流程
  - 定义Release group
  - 定义Release code
  - 定义Release indictor
  - 定义Release Strategy
  - 建立分类Z_PUR_DOC_RELEASE
- Stock Transfer Order
- MM PO配置
- 跨公司transfer order
- 两种外包方式比较
  - 业务背景
  - 直接使用外包PO
  - 使用工单混合作业外包
  - 委外加工的种类和处理方法(使用prod. Order和purchase order)
- MM Condition MM采购定价
- 透视条件（Condition）技术
  - 定义采购定价控制级别（SE16：V_001W_K）
  - 熟悉采购定价过程
- 物料主数据
  - 物料主数据配置
  - 为用户设置可维护主数据屏幕
  - 限制维护物料字段
  - 设置物料交易状态（Tcode：OMS4）
  - 特殊物料处理
- SAP相关打印编程- PO打印
- 物料管理(Material Management) 后台配置
  - 物料管理一般设置
  - 采购环境数据(Environment Data)
  - 物料采购数据(Material Data)
  - 分隔评估(Split Valuation)
  - 供应商和合作伙伴确定(Vendor Master| Parter Determination)
  - 后勤发票校验(Logistics Invoice Verification)
  - 收进发票处理(Incoming Invoice)
  - Valuation and Account Assignment
  - 例1：如何使用Valuation group code
  - 例2：PO condition和OBYC
  - 例3：移动类型如何取得自动配置科目？
  - 运杂费处理
  - GR/IR科目拆分
  - 物料类型
  - 管道物料(Pipeline Material)
  - 供应商寄存物料(Consignment Stock)
  - 委外加工物资
  - 寄售给客户物料
  - 客户维修物料
  - 更改物料Valuation class
  - GR/IR 的绝妙应用

### 14. PP - Production
- 使用外包工序
  - 建立作业外包信息记录
  - 建立外包工序
  - 外包标准成本估算
  - 建立外包工单
  - 外包采购单收货
  - 外包工单收货外包件价格设置
- Super BOM(Configurable material BOM)的应用
  - Classification System(分类系统)简介
  - Super BOM和配置BOM应用举例
  - 建立物料(Tcode:MM01)
  - 建立Super BOM(CS01)
  - 建立configurable profile (Tcode:CU41)
  - 例1-Phantom Part的使用
  - 例2 配置BOM的成本估算

### 15. SD - Sales & Distribution
- SD Condition SD销售定价

### 16. BC - Basis
- How to Archive material master data or inventory data?
- Relatd T-codes
- How to change valuation category with existed transaction data
- How to archive the batch data
- Unit test OK!
- How to delete a change request
- How to set required fields for material master
  - Self define a Sel. Group and Re-assign Fields to Field Selection Groups
  - Maintain Field Selection for Data Screens
  - Unit test result
- Little SAP tips
- How to add a search Help?
  - What is so-called a search help
  - How to add a search help for material master data
- How to add code for SAP Query
  - Case 1：change fields sign
  - Case 2：Add additional Tables and fields
  - Case 3：Coding using work area or internal table for additional fields
  - Case 4：Use alias table to add a same table for query twice or multiple times
  - Case5：User cluster table BSEG with logical database
  - Case6：Use left outer join to avoid query data missing
  - Case7：Change Query Program with SE38
- 大话ERP权限控制
- IMG剖析和SE16
- 如何收集常用事务码?

### 17. ABAP
- ABAP开发三月通
  - 前言
  - 基础篇
  - 加强篇
  - 实战篇
  - MM模块开发实例
  - SD模块开发实例
  - PP模块开发实例
  - FI模块开发实例
  - CO模块开发实例
  - Basis相关开发实例
  - 开发项目流程简介
  - 附录
  - ABAPer 常用Tcode
  - 编写用户增强
  - 操作最简单的欺骗Access Key的文档

### 18. BW
- 第一篇 BW篇
  - 第1

## 下载链接

[SAP屠夫作品汇总分享](https://pan.quark.cn/s/b077cc163760)