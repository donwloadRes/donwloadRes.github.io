---
layout: post
title: "基于STM32的无接触测温并在OLED显示的代码"
date:   2024-04-27
tags: [STM32,OLED,测温,代码,库函数]
comments: true
author: admin
---
# 基于STM32的无接触测温并在OLED显示的代码

## 项目描述

本项目提供了一个基于STM32F103C8T6微控制器的无接触测温系统代码。该系统通过GY-906红外测温模块进行温度测量，并将测量结果显示在OLED屏幕上。代码使用STM32的库函数进行编写，方便用户快速理解和使用。

## 功能特点

- **无接触测温**：通过GY-906红外测温模块实现非接触式温度测量。
- **OLED显示**：测量结果实时显示在OLED屏幕上，方便用户查看。
- **STM32库函数**：代码基于STM32的库函数编写，易于理解和修改。

## 硬件需求

- STM32F103C8T6微控制器
- GY-906红外测温模块
- OLED显示屏
- 电源模块
- 连接线

## 软件需求

- Keil uVision或其他STM32开发环境
- STM32库函数

## 使用说明

1. **硬件连接**：
   - 将GY-906模块与STM32的I2C接口连接。
   - 将OLED显示屏与STM32的SPI或I2C接口连接。
   - 确保所有连接正确无误。

2. **软件配置**：
   - 打开Keil uVision或其他STM32开发环境。
   - 导入本项目提供的代码。
   - 根据硬件连接配置I2C或SPI接口。
   - 编译并下载代码到STM32微控制器。

3. **运行测试**：
   - 上电后，系统将自动开始测温。
   - 测量结果将实时显示在OLED屏幕上。

## 注意事项

- 请确保硬件连接正确，避免短路或连接错误导致设备损坏。
- 代码中使用的I2C或SPI接口可根据实际硬件进行调整。
- 如有任何问题，请参考STM32的官方文档或联系开发者。

## 贡献

欢迎对本项目进行改进和优化，如有任何建议或问题，请提交Issue或Pull Request。

## 许可证

本项目代码遵循MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[基于STM32的无接触测温并在OLED显示的代码](https://pan.quark.cn/s/3081d02f54ef)