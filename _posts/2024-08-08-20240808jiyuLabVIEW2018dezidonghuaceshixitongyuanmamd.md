---
layout: post
title: "基于LabVIEW 2018的自动化测试系统源码"
date:   2022-06-02
tags: [测试,源码,用户,LabVIEW,OOP]
comments: true
author: admin
---
# 基于LabVIEW 2018的自动化测试系统源码

## 简介

本资源文件提供了一套基于LabVIEW 2018开发的自动化测试系统源码。该系统模仿TestStand编写，旨在帮助使用者快速上手自动化测试系统的开发，无需花费大量时间学习TestStand。源码采用状态机编程，未涉及面向对象编程（OOP），因此用户无需熟悉OOP知识，只需了解状态机编程即可。

## 功能特点

1. **多路并行测试**：
   - 支持两路测试同时进行。
   - 三路及以上的并行测试可根据需求定制开发。

2. **测试过程控制**：
   - 测试过程中可随时暂停和继续。

3. **测试报告生成**：
   - 支持生成Word或PDF格式的测试报告。

4. **数据存储与管理**：
   - 测试参数及数据存储于SQL Server数据库中。
   - 可调阅历史测试数据和报告。

5. **用户管理与权限控制**：
   - 具备用户登录和用户管理功能。
   - 支持最多十级权限设置。

6. **测试工况参数管理**：
   - 可添加不同产品的测试工况参数。
   - 测试步骤的判定条件支持添加、删除、插入和修改。

## 使用说明

1. **环境要求**：
   - LabVIEW 2018及以上版本。
   - SQL Server数据库。

2. **开发与修改**：
   - 本源码为示例程序，用户需根据实际需求进行局部修改。
   - 建议用户具备一定的LabVIEW编程基础，特别是状态机编程的相关知识。

3. **数据库配置**：
   - 用户需根据实际情况配置SQL Server数据库，确保测试数据和报告的存储与读取正常。

4. **用户权限管理**：
   - 可根据项目需求设置不同级别的用户权限，确保系统的安全性。

## 注意事项

- 本源码未涉及面向对象编程（OOP），用户无需熟悉OOP知识。
- 测试系统的具体功能和参数需根据实际需求进行调整和优化。

## 联系我们

如有任何问题或建议，欢迎通过GitHub Issues或Pull Requests与我们联系。

## 下载链接

[基于LabVIEW2018的自动化测试系统源码](https://pan.quark.cn/s/28ada73e4b68)