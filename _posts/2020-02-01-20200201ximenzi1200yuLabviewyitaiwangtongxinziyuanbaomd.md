---
layout: post
title: "西门子1200与Labview以太网通信资源包"
date:   2020-12-08
tags: [Labview,PLC,1200,程序,西门子]
comments: true
author: admin
---
# 西门子1200与Labview以太网通信资源包

## 资源描述

本资源包提供了西门子1200 PLC与Labview通过以太网进行通信的完整解决方案。资源包内包含Labview程序和1200 PLC程序，经过实际测试，确保通信功能正常运行。

## 主要内容

- **Labview程序**：用于与西门子1200 PLC进行数据通信的Labview程序。
- **1200 PLC程序**：用于与Labview进行数据通信的西门子1200 PLC程序。
- **详细配置说明**：包括如何配置PLC和Labview以实现通信的详细步骤。

## 使用说明

1. **PLC配置**：
   - 在PLC程序中，确保将OB1中的TSEND_C组态中的IP地址192.168.0.11修改为你自己电脑的IP地址。
   - M0.0是开关，当M0.0为true时，PLC将开始发送数据给Labview。

2. **Labview配置**：
   - 打开Labview程序，按照配置说明进行设置，确保与PLC的IP地址一致。
   - 运行Labview程序，开始接收来自PLC的数据。

## 适用对象

本资源包非常适合初学者使用，无论是学习PLC编程还是Labview通信，都能从中获得实用的知识和经验。

## 下载说明

请点击下载按钮获取资源包，解压后按照说明进行配置和使用。

欢迎下载并使用本资源包，祝你学习顺利！

## 下载链接

[西门子1200与Labview以太网通信资源包](https://pan.quark.cn/s/25d11343e6ea)