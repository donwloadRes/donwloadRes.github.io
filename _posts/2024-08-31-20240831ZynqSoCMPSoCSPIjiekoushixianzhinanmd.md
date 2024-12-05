---
layout: post
title: "Zynq SoC-MPSoC SPI接口实现指南"
date:   2020-11-17
tags: [SPI,控制器,PS,PL,实现]
comments: true
author: admin
---
# Zynq SoC/MPSoC SPI接口实现指南

## 资源文件介绍

### 文件名
pg153-axi-quad-spi.pdf

### 文件描述

在设计中使用Zynq SoC或Zynq UltraScale + MPSoC时，实现SPI接口有两种主要方法：

1. **使用PS端的SPI控制器**：PS端提供了两个SPI控制器，可以直接使用这些控制器来实现SPI通信。
2. **在PL端使用AXI Quad SPI (QSPI) IP模块**：通过配置PL端的AXI Quad SPI IP模块，可以实现标准的SPI通信。

根据应用的具体需求，可以选择其中一种方法来实现SPI控制器。这两种方法都支持四种SPI模式，并且都可以作为SPI主设备或SPI从设备。

### 差异对比

下表列出了这两种SPI实现方式之间的一些主要差异：

| 特性           | PS端SPI控制器 | PL端AXI Quad SPI |
|----------------|----------------|-------------------|
| 位置           | PS端           | PL端              |
| 控制器数量     | 2个            | 1个               |
| 配置复杂度     | 较低           | 较高              |
| 性能           | 中等           | 较高              |
| 资源占用       | 较低           | 较高              |
| 灵活性         | 中等           | 较高              |

通过这份资源文件，您可以深入了解这两种SPI实现方式的详细信息，并根据您的项目需求选择最合适的方案。

## 下载链接

[ZynqSoCMPSoCSPI接口实现指南](https://pan.quark.cn/s/935095bdb991)