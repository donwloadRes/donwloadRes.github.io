---
layout: post
title: "基于STM32单片机在OLED上显示DHT11温湿度"
date:   2023-08-03
tags: [STM32,OLED,引脚,DHT11,温湿度]
comments: true
author: admin
---
# 基于STM32单片机在OLED上显示DHT11温湿度

## 项目简介

本项目使用STM32F103C8T6最小核心板和DHT11温湿度传感器，通过STM32单片机实时采集DHT11传感器检测到的温湿度数据，并将这些数据实时显示在OLED屏幕上。通过本项目，您可以学习如何使用STM32单片机进行传感器数据采集和显示，以及如何驱动OLED屏幕。

## 项目功能

- **温湿度数据采集**：通过DHT11传感器实时采集环境中的温度和湿度数据。
- **数据处理与显示**：将采集到的温湿度数据通过STM32单片机进行处理，并将处理后的数据显示在OLED屏幕上。
- **实时更新**：OLED屏幕上的数据显示会实时更新，确保用户能够看到最新的温湿度信息。

## 硬件需求

- STM32F103C8T6最小核心板
- DHT11温湿度传感器
- OLED屏幕（I2C接口）
- 杜邦线若干
- 面包板（可选）

## 软件需求

- Keil uVision（或其他STM32开发环境）
- STM32 HAL库

## 项目结构

- `src/`：包含项目的源代码文件。
- `inc/`：包含项目的头文件。
- `README.md`：项目说明文件。

## 使用说明

1. **硬件连接**：
   - 将DHT11传感器的VCC引脚连接到STM32的3.3V电源。
   - 将DHT11传感器的GND引脚连接到STM32的GND。
   - 将DHT11传感器的DATA引脚连接到STM32的任意一个GPIO引脚（例如PA0）。
   - 将OLED屏幕的VCC引脚连接到STM32的3.3V电源。
   - 将OLED屏幕的GND引脚连接到STM32的GND。
   - 将OLED屏幕的SCL引脚连接到STM32的I2C时钟线（例如PB6）。
   - 将OLED屏幕的SDA引脚连接到STM32的I2C数据线（例如PB7）。

2. **软件配置**：
   - 打开Keil uVision，导入项目文件。
   - 配置STM32的GPIO引脚和I2C接口。
   - 编译并下载程序到STM32单片机。

3. **运行项目**：
   - 程序下载完成后，STM32单片机会自动开始采集DHT11传感器的温湿度数据，并将数据显示在OLED屏幕上。

## 注意事项

- 确保DHT11传感器和OLED屏幕的电源电压为3.3V，避免电压不匹配导致设备损坏。
- 在连接硬件时，注意引脚的正确连接，避免短路。
- 如果OLED屏幕无法正常显示，请检查I2C接口的配置是否正确。

## 贡献

欢迎对本项目进行改进和优化，如果您有任何建议或发现了问题，请提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅`LICENSE`文件。

## 下载链接

[基于STM32单片机在OLED上显示DHT11温湿度](https://pan.quark.cn/s/60663bb382c5)