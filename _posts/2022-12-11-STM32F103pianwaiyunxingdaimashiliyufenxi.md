---
layout: post
title: "STM32F103片外运行代码示例与分析"
date:   2024-11-28
tags: [片外,SRAM,BootLoader,NorFlash,应用程序]
comments: true
author: admin
---
# STM32F103片外运行代码示例与分析

## 简介
本资源文件提供了在KEIL开发环境下，如何在STM32F103微控制器上实现程序在片外NorFlash或SRAM中运行的示例代码与分析。STM32F103系列微控制器支持三种启动方式，但默认情况下无法直接在片外NorFlash或SRAM中启动程序。因此，本示例通过使用BootLoader来实现这一功能。

## 资源内容
本资源包含以下三个文件夹：

1. **BOOT**：包含BootLoader的代码，该BootLoader被放置在片内Flash中。启动后，BootLoader会配置FSMC_SRAM和FSMC_NOR，并执行跳转操作，使程序能够在片外运行。

2. **NorFlash应用程序**：包含在片外NorFlash中运行的应用程序代码。

3. **SRAM应用程序**：包含在片外SRAM中运行的应用程序代码。

## 开发环境
所有代码均采用KEIL 3.8版本进行编译。

## 使用说明
1. **编译BootLoader**：首先编译BOOT文件夹中的BootLoader代码，并将其烧录到STM32F103的片内Flash中。

2. **编译应用程序**：根据需要在NorFlash或SRAM中运行程序，选择相应的应用程序文件夹进行编译。

3. **烧录应用程序**：将编译好的应用程序烧录到片外NorFlash或SRAM中。

4. **启动运行**：上电后，STM32F103会首先运行片内Flash中的BootLoader，BootLoader会配置FSMC并跳转到片外NorFlash或SRAM中执行应用程序。

## 注意事项
- 确保BootLoader和应用程序的地址配置正确，以避免跳转失败。
- 在配置FSMC时，注意时序参数的设置，以确保片外存储器的正常访问。

## 总结
通过本资源，您可以学习如何在STM32F103上实现程序在片外NorFlash或SRAM中运行的方法。希望这些示例代码和分析对您的开发工作有所帮助。

## 下载链接

[STM32F103片外运行代码示例与分析](https://pan.quark.cn/s/6a047931a738)