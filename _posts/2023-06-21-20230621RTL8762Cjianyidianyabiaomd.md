---
layout: post
title: "RTL8762C 简易电压表"
date:   2024-10-30
tags: [RTL8762C,电压,蓝牙,电压表,电路设计]
comments: true
author: admin
---
# RTL8762C 简易电压表

## 项目描述

本项目使用RTL8762C芯片，通过ADC和SPI接口实现了一个简易的电压表功能。该电压表可以通过蓝牙订阅实时查看电压值。由于项目在电路设计上未做过多考虑，因此仅能监测3.3V以下的电压。功能较为简单，代码编写仓促，结构也不尽合理，主要用于学习目的。

## 功能特点

- **电压监测**：通过ADC采集电压值，实现对3.3V以下电压的监测。
- **蓝牙实时查看**：通过蓝牙连接，可以实时订阅并查看电压值。

## 使用说明

1. **硬件连接**：将RTL8762C芯片与所需的外设（如ADC、SPI接口）正确连接。
2. **编译与烧录**：使用相应的开发工具编译代码，并将生成的固件烧录到RTL8762C芯片中。
3. **蓝牙连接**：使用支持蓝牙的设备（如手机、电脑）连接到RTL8762C芯片，订阅电压值。

## 注意事项

- 本项目仅适用于学习目的，电路设计和代码结构较为简陋，不建议用于实际应用。
- 由于电路设计限制，仅能监测3.3V以下的电压，请勿用于高电压环境。

## 贡献

欢迎对本项目提出改进建议或提交代码优化，共同学习与进步。

## 许可证

本项目采用开源许可证，具体许可证类型请参考项目根目录下的LICENSE文件。

## 下载链接

[RTL8762C简易电压表](https://pan.quark.cn/s/c795f2e14579)