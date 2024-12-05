---
layout: post
title: "STM32CubeMX HAL库 UART串口接收中断回调函数代码分析"
date:   2021-07-22
tags: [HAL,串口,UART,回调,STM32CubeMX]
comments: true
author: admin
---
# STM32CubeMX HAL库 UART串口接收中断回调函数代码分析

## 资源文件介绍

### 文件名
STM32CubeMX-HAL库-UART串口接收中断回调函数代码分析.docx

### 文件描述
本文档详细分析了在STM32CubeMX中使用HAL库进行UART串口通信时，中断回调函数的调用机制。通过对比传统库函数调用与HAL库中的回调函数调用，帮助读者理解HAL库中中断处理的不同之处。

在学习和使用STM32CubeMX进行串口通信时，许多开发者可能会对HAL库中的回调函数感到困惑，不清楚这些回调函数是如何被调用的。本文通过深入分析每个回调函数的定义，并结合实际工程代码，帮助读者理清HAL库中断调用的流程。

本文不仅旨在加深作者自身的理解，也希望为那些对HAL库中回调函数调用机制感到困惑的朋友提供帮助。

### 参考工程
本文的分析基于以下工程代码：
【STM32】-CubeMX-HAL库-UART-串口通信-STM32F103C8T6-收发测试

通过阅读本文档，您将能够更好地理解STM32CubeMX中HAL库的UART串口通信机制，特别是中断回调函数的调用流程。

## 下载链接

[STM32CubeMXHAL库UART串口接收中断回调函数代码分析](https://pan.quark.cn/s/ed7ec198ca46)