---
layout: post
title: "IAR程序调试方法说明"
date:   2020-07-01
tags: [SPY,程序调试,IAR,调试,文档]
comments: true
author: admin
---
# IAR程序调试方法说明

## 资源文件介绍

本仓库提供了一个名为“IAR程序调试方法说明.doc”的资源文件，该文件详细介绍了如何在IAR Embedded Workbench IDE中使用C-SPY调试工具进行程序调试。

## 文件内容概述

IAR Embedded Workbench IDE集成了功能丰富的程序调试工具——C-SPY。C-SPY可以通过多种方式连接不同的目标系统，甚至自带了纯软件的模拟器（Simulator），使得在没有硬件系统的情况下也能进行程序调试。C-SPY不仅支持单步、断点、变量和表达式监测、寄存器和堆栈信息查看等基本调试功能，还支持反汇编等其他特性。

相对于传统的打印日志调试方式，使用C-SPY调试工具具有更直观、更高效且不依赖于串口等优势。

## 调试方法说明

本文档主要针对C-SPY通过J-LINK工具连接AD7028S设备这种STM32平台的调试方法进行了入门式的简要说明。对于非STM32平台的调试方法，虽然与本文档所述类似，但本文不做另外说明。

## 学习资源

如果想要系统性地学习C-SPY调试工具，可以通过以下路径查阅官方文档：

1. 打开IAR Embedded Workbench IDE。
2. 点击菜单栏中的“Help”。
3. 选择“C-SPY Debugging Guide”。

## 注意事项

本文档仅作为入门指南，详细的功能和使用方法请参考官方文档。

## 下载链接

[IAR程序调试方法说明分享](https://pan.quark.cn/s/1ac84b721fe7)