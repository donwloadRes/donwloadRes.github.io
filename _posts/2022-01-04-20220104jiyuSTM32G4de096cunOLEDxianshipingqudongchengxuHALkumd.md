---
layout: post
title: "基于STM32G4的0.96寸OLED显示屏驱动程序（HAL库）"
date:   2024-03-30
tags: [I2C,OLED,驱动程序,0.96,define]
comments: true
author: admin
---
# 基于STM32G4的0.96寸OLED显示屏驱动程序（HAL库）

## 简介

本项目提供了一个基于STM32G4系列微控制器的0.96寸OLED显示屏驱动程序，使用HAL库进行开发。该驱动程序支持硬件I2C和软件I2C两种通信方式，适用于多种应用场景。

## 功能特点

- **支持硬件I2C和软件I2C**：用户可以根据需求选择使用硬件I2C或软件I2C进行通信。
- **多种显示内容**：支持显示英文、整数、浮点数、汉字、图像、二进制数、十六进制数等内容。
- **图形绘制功能**：支持画点、直线、矩形、圆、椭圆、三角形等基本图形。
- **多种字体支持**：提供多种字体选择，满足不同显示需求。
- **简易图形库**：功能丰富，相当于一个简易版的图形库。

## 使用说明

### 硬件配置

- **开发板**：NUCLEO-G474RE
- **OLED模块**：0.96寸OLED显示屏，4针脚I2C接口

### 软件配置

1. **STM32CubeMX配置**：
   - 设置I2C外设引脚，配置为SCL和SDA。
   - 启用对应的I2C外设，设置速度模式为Fast Mode Plus，速度为1000。
   - 配置GPIO引脚为复用开漏输出模式，设置IO输出速度为Very High。

2. **代码配置**：
   - 在`OLED.c`文件中，根据需要选择使用硬件I2C或软件I2C。
   - 如果使用硬件I2C，取消注释`#define OLED_USE_HW_I2C`，并注释掉`#define OLED_USE_SW_I2C`。
   - 如果使用软件I2C，取消注释`#define OLED_USE_SW_I2C`，并注释掉`#define OLED_USE_HW_I2C`。

### 编译与下载

- 使用Keil5或Vscode+EIDE进行编译和下载。
- 工程文件使用UTF-8编码，确保编辑器编码设置为UTF-8。

## 参考资料

- 关于OLED的驱动原理及驱动程序的使用教程，可以参考江协科技的相关视频。
- 更多关于STM32的I2C相关信息和使用方法，可以参考相关技术文档。

## 联系我们

如有任何问题或建议，欢迎通过邮件联系我们：feedback@jiangxiekeji.com

---

**版权声明**：本文为博主原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[基于STM32G4的0.96寸OLED显示屏驱动程序HAL库](https://pan.quark.cn/s/26ace51d4ced)