---
layout: post
title: "STM32F103 ISP串口下载程序学习笔记"
date:   2022-12-14
tags: [ISP,下载,串口,BOOT0,BOOT1]
comments: true
author: admin
---
# STM32F103 ISP串口下载程序学习笔记

## 简介
本资源文件详细介绍了如何在STM32F103系列微控制器上使用ISP（In-System Programming）通过串口下载程序。ISP允许用户在电路板上直接对空白器件进行编程，而不需要将器件从电路板上取下。已经编程的器件也可以通过ISP方式擦除或再编程。

## 主要内容

### 1. ISP概述
- **ISP（In-System Programming）**：在系统可编程，指电路板上的空白器件可以编程写入最终用户代码，而不需要从电路板上取下器件。已经编程的器件也可以用ISP方式擦除或再编程。
- **Bootloader**：ISP时需要用到自举程序（Bootloader），自举程序存储在STM32器件的内部自举ROM存储器（系统存储器）中。其主要任务是通过可用的串行外设（如USART、CAN、USB、I2C等）将应用程序下载到内部Flash中。

### 2. BOOT配置
- **BOOT0和BOOT1配置**：通过设置BOOT0和BOOT1的电平，可以选择不同的启动模式。例如，BOOT0为高电平，BOOT1为低电平时，单片机进入bootloader模式，可以通过串口下载程序。

### 3. 串口下载程序
- **下载工具**：推荐使用mcuisp v0.993进行串口下载。
- **操作步骤**：
  1. 电脑通过USB转串口线连接STM32的USART1。
  2. 打开电脑端的上位机，设置跳线保持BOOT0为高电平，BOOT1为低电平。
  3. 复位单片机使其进入bootloader模式。
  4. 通过上位机下载程序。
  5. 下载完毕后，设置跳线保持BOOT0为低电平，BOOT1为低电平，复位单片机即可启动用户代码，正常运行。

## 注意事项
- 在下载程序时，确保BOOT0和BOOT1的电平设置正确，否则可能导致无法进入bootloader模式。
- 使用mcuisp工具时，建议设置波特率为115200，以确保下载过程的稳定性。

## 总结
通过本资源文件的学习，用户可以掌握如何在STM32F103系列微控制器上使用ISP通过串口下载程序。这对于开发和调试STM32项目具有重要意义。

## 下载链接

[STM32F103ISP串口下载程序学习笔记](https://pan.quark.cn/s/3aef705376f0)