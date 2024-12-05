---
layout: post
title: "STM32F103ZET6 驱动43英寸TFT LCD彩色液晶触摸屏例程"
date:   2020-05-03
tags: [TFT,LCD,4.3,例程,触摸屏]
comments: true
author: admin
---
# STM32F103ZET6 驱动4.3英寸TFT LCD彩色液晶触摸屏例程

## 资源描述

本仓库提供了一个STM32F103ZET6微控制器驱动4.3英寸TFT LCD彩色液晶触摸屏的例程。该例程详细展示了如何使用STM32微控制器驱动TFT LCD显示屏，并实现触摸功能。

## 资源文件

- **文件名**: STM32F103ZET6-TFTLCD-TOUCH-4.3INCH.rar
- **文件描述**: 该文件包含了STM32驱动4.3英寸TFT LCD彩色液晶触摸屏的完整例程。TFT LCD采用16位8080并口驱动芯片NT35510，触摸屏触摸芯片为I2C总线GT968/GT1151。本例程将正点原子KEIL工程例程移植到STM32CUBEIDE工程环境。

## 例程特点

1. **TFT LCD驱动**: 使用NT35510芯片驱动4.3英寸TFT LCD，支持16位8080并口通信。
2. **触摸屏驱动**: 使用GT968/GT1151触摸芯片，通过I2C总线实现触摸功能。
3. **工程移植**: 将正点原子的KEIL工程成功移植到STM32CUBEIDE工程环境，方便用户在STM32CUBEIDE中进行开发和调试。

## 使用说明

1. **解压文件**: 下载并解压`STM32F103ZET6-TFTLCD-TOUCH-4.3INCH.rar`文件。
2. **导入工程**: 将解压后的工程文件导入到STM32CUBEIDE中。
3. **编译与下载**: 编译工程并下载到STM32F103ZET6开发板上。
4. **调试与运行**: 连接4.3英寸TFT LCD显示屏和触摸屏，运行程序并进行调试。

## 相关文档

关于本例程的详细介绍和使用方法，请参考CSDN博文《STM32 驱动4.3寸TFT LCD 触摸屏》。

## 注意事项

- 请确保硬件连接正确，特别是TFT LCD和触摸屏的接口。
- 在编译和下载程序时，请确保STM32CUBEIDE环境配置正确。

## 联系我们

如有任何问题或建议，欢迎通过GitHub Issues或邮件联系我们。

## 下载链接

[STM32F103ZET6驱动4.3英寸TFTLCD彩色液晶触摸屏例程](https://pan.quark.cn/s/d8622a1f3e43)