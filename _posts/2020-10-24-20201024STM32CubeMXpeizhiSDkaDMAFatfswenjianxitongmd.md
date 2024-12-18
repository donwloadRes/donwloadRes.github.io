---
layout: post
title: "STM32CubeMX配置SD卡DMAFatfs文件系统"
date:   2021-09-24
tags: [SD,配置,DMA,Fatfs,文件系统]
comments: true
author: admin
---
# STM32CubeMX配置SD卡+DMA+Fatfs文件系统

本资源文件详细介绍了如何使用STM32CubeMX配置SD卡、DMA和Fatfs文件系统，适用于STM32F407探索者开发板。通过本教程，您可以学习如何在STM32微控制器上实现SD卡的读写操作，并使用Fatfs文件系统进行文件管理。

## 设备及软件
1. **Keil**：用于编写和编译代码。
2. **STM32CubeMX**：用于配置STM32微控制器的硬件资源。
3. **正点原子STM32F407探索者开发板**：本教程使用的硬件平台。

## 配置步骤
1. **配置RCC外部晶振和SYS为SW模式**：确保系统时钟和外部晶振正确配置。
2. **配置USART1**：用于调试信息的输出。
3. **时钟树配置**：设置SDIO模块输入时钟为48MHz。
4. **SDIO配置**：配置SDIO时钟为12MHz，打开SDIO中断，并添加DMA支持。
5. **配置Fatfs文件系统**：支持中文及长文件名，使用DMA模板，配置SD卡插入检测引脚。
6. **配置NVIC**：设置SDIO中断优先级大于DMA。
7. **生成代码配置**：必须加大堆栈内存，否则可能不够。
8. **生成代码**：生成Keil工程文件。

## 修改代码
1. **修改BSP_SD_IsDetected函数**：由于探索者开发板没有SD卡检测引脚，需要修改该函数。
2. **修改USART代码**：添加必要的初始化代码。
3. **修改主函数测试代码**：添加Fatfs文件系统的读写测试代码。

## 打印测试
成功配置并运行后，系统将能够正确读写SD卡中的文件，并通过USART输出调试信息。

## 注意事项
1. **堆栈内存**：必须加大堆栈内存，否则可能导致程序运行不稳定。
2. **SD卡检测引脚**：探索者开发板不带SD卡检测引脚，需手动配置一个引脚并生成工程后注释相关代码。

通过本教程，您将掌握如何在STM32微控制器上配置和使用SD卡、DMA和Fatfs文件系统，为后续的嵌入式开发打下坚实基础。

## 下载链接

[STM32CubeMX配置SD卡DMAFatfs文件系统](https://pan.quark.cn/s/839e464cd2fa)