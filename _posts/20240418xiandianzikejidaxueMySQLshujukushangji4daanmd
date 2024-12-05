---
layout: post
title: "西安电子科技大学MySQL数据库上机4答案"
date:   2022-06-21
tags: [int,String,预订,航班,大巴车]
comments: true
author: admin
---
# 西安电子科技大学MySQL数据库上机4答案

## 资源描述

本资源文件提供了西安电子科技大学MySQL数据库上机4的答案。题目要求基于MySQL设计并实现一个简单的旅行预订系统，涉及航班、大巴班车、宾馆房间和客户数据等信息。以下是题干内容，答案在文件中。

### 题目要求

#### 关系模式

- **FLIGHTS**: 航班信息表
  - `flightNum` (String): 航班号
  - `price` (int): 价格
  - `numSeats` (int): 座位总数
  - `numAvail` (int): 可用座位数
  - `FromCity` (String): 出发城市
  - `ArivCity` (String): 到达城市

- **HOTELS**: 宾馆信息表
  - `location` (String): 地点
  - `price` (int): 价格
  - `numRooms` (int): 房间总数
  - `numAvail` (int): 可用房间数

- **BUS**: 大巴信息表
  - `location` (String): 地点
  - `price` (int): 价格
  - `numBus` (int): 大巴总数
  - `numAvail` (int): 可用大巴数

- **CUSTOMERS**: 客户信息表
  - `custName` (String): 客户姓名
  - `custID` (String): 客户ID

- **RESERVATIONS**: 预订信息表
  - `custName` (String): 客户姓名
  - `resvType` (int): 预订类型（1为航班，2为宾馆房间，3为大巴车）
  - `resvKey` (String): 预订关键字

#### 假设条件

1. 在给定的一个班机上，所有的座位价格也一样；`flightNum`是表`FLIGHTS`的一个主码。
2. 在同一个地方的所有的宾馆房间价格也一样；`location`是表`HOTELS`的一个主码。
3. 在同一个地方的所有大巴车价格一样；`location`是表`BUS`的一个主码。
4. `custName`是表`CUSTOMERS`的一个主码。
5. 表`RESERVATIONS`包含着那些和客户预订的航班、大巴车或宾馆房间相应的条目，具体的说，`resvType`指出预订的类型（1为预订航班，2为预订宾馆房间，3为预订大巴车），而`resvKey`是表`RESERVATIONS`的一个主码。
6. 在表`FLIGHTS`中，`numAvail`表示指定航班上的还可以被预订的座位数。对于一个给定的航班（`flightNum`）数据库一致性的条件之一是，表`RESERVATIONS`中所有预订该航班的条目数加上该航班的剩余座位数必须等于该航班上总的座位数。这个条件对于表`BUS`和表`HOTELS`同样适用。

#### 功能要求

1. 航班、大巴车、宾馆房间和客户基础数据的入库和更新。
2. 预定航班、大巴车、宾馆房间。
3. 查询航班、大巴车、宾馆房间、客户和预订信息。
4. 查询某个客户的旅行线路。
5. 检查预定线路的完整性。
6. 其他任意你愿意加上的功能。

## 使用说明

1. **下载文件**: 下载本仓库中的资源文件，文件中包含了完整的答案和实现代码。
2. **导入数据库**: 将提供的SQL文件导入到你的MySQL数据库中。
3. **运行代码**: 根据题目要求，运行相应的SQL查询和操作，验证系统的功能。

## 注意事项

- 请确保你的MySQL数据库版本与代码兼容。
- 在运行代码之前，建议先备份你的数据库，以防数据丢失。

## 贡献

如果你有任何改进或建议，欢迎提交Pull Request或Issue。

## 许可证

本资源文件遵循MIT许可证。详情请参阅LICENSE文件。

## 下载链接

[西安电子科技大学MySQL数据库上机4答案分享](https://pan.quark.cn/s/e524fcc5ce54)