---
layout: post
title: "STM32与K210-OpenMV串口通信+源码"
date:   2022-10-20
tags: [串口,STM32,K210,OpenMV,通信]
comments: true
author: admin
---
# STM32与K210/OpenMV串口通信+源码

## 资源描述

本仓库提供了一个完整的STM32与K210/OpenMV串口通信的示例项目，包含STM32、K210和OpenMV的源代码。通过本项目，您可以快速入门STM32的串口通信，并实现STM32与K210/OpenMV之间的数据传输。

## 文件结构

- `stm32串口调试.zip`: STM32端的代码，包含串口通信的实现和OLED显示功能。
- `k210.py`: K210端的代码，实现串口通信并交替发送字符"a"和"b"。
- `openmv.py`: OpenMV端的代码，实现串口通信并交替发送字符"a"和"b"。

## 引脚定义

### STM32端

- **四脚I2C OLED**:
  - SCL -> B12
  - SDA -> B13
- **串口1**:
  - TX -> A9
  - RX -> A10
  - 波特率: 9600
- **功能**: 接收数据并显示在OLED上。

### K210端

- **串口1**:
  - TX -> 15
  - RX -> 16
  - 波特率: 9600
- **功能**: 交替发送字符"a"和"b"。

### OpenMV端

- **串口3**:
  - TX -> P4
  - RX -> P5
  - 波特率: 9600
- **功能**: 交替发送字符"a"和"b"。

## 适用场景

本项目适用于以下场景：

- STM32与K210之间的串口通信。
- STM32与OpenMV之间的串口通信。

通过本项目，您可以快速搭建STM32与K210/OpenMV之间的通信系统，并实现数据的传输与显示。

## 下载链接

[STM32与K210OpenMV串口通信源码](https://pan.quark.cn/s/29fae318e242)