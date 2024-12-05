---
layout: post
title: "AUTOSAR入门指南：CAN网络管理详解"
date:   2023-12-05
tags: [节点,Sleep,Bus,Mode,总线]
comments: true
author: admin
---
# AUTOSAR入门指南：CAN网络管理详解

## 资源文件介绍

本仓库提供了一个名为“AUTOSAR入门.pdf”的资源文件，该文件详细介绍了AUTOSAR（汽车开放系统架构）中的CAN网络管理（CanNM）模块。CanNM模块主要用于管理CAN总线上的网络通信，确保节点在需要时保持通信，并在不需要时进入低功耗模式以节省能量。

## 文件内容概述

### 核心思想

1. **保持通信**：如果节点需要保持通信，则节点需要周期性地发送NMPDUs（网络管理协议数据单元），否则停止发送NMPDUs。
2. **总线休眠**：如果总线上的所有节点不需要使用总线，那么总线上过了一段时间没有NMPDUs时，则会进入Bus-Sleep Mode。

### 工作模式和状态

CanNm模块一共有三种工作模式：

1. **Network Mode**
   - **Repeat Message State**：用于确保从Bus-Sleep或Prepare Bus-Sleep到Network Mode的节点被总线上其他节点发现。
   - **Normal Operation State**：保持总线处于唤醒状态，节点在此状态下发送NMPDUs。
   - **Ready Sleep State**：节点准备释放总线，等待其他节点进入Prepare Bus-Sleep Mode。

2. **Prepare Bus-Sleep Mode**：等待总线上的所有节点能够在进入Bus-Sleep Mode之前，有时间停止节点的active状态。

3. **Bus-Sleep Mode**：当没有消息被传送时，减少能量的消耗。节点可以被本地唤醒源或CAN线唤醒源唤醒。

### 模式切换

模式的改变应该通过回调函数通知上层应用。例如，当节点进入Bus-Sleep Mode时，应通知上层应用。

## 适用人群

本资源文件适合以下人群阅读：

- 汽车电子工程师
- AUTOSAR系统开发人员
- CAN网络管理模块的初学者和进阶学习者

## 使用说明

1. 下载“AUTOSAR入门.pdf”文件。
2. 打开文件，详细阅读CanNM模块的工作原理和状态转换机制。
3. 根据实际项目需求，参考文件中的内容进行CAN网络管理模块的配置和开发。

## 版权声明

本文内容基于CSDN博主“cococenstar”的原创文章，遵循CC 4.0 BY-SA版权协议。转载请附上原文出处链接及本声明。

---

希望这份指南能帮助你更好地理解和应用AUTOSAR中的CAN网络管理模块。如果有任何问题或建议，欢迎在仓库中提出。

## 下载链接

[AUTOSAR入门指南CAN网络管理详解](https://pan.quark.cn/s/1e9c5e9bbb56)