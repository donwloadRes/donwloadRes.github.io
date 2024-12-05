---
layout: post
title: "STM32F1 ESP8266 TCP透传程序"
date:   2023-08-04
tags: [SmartConfig,ESP8266,透传,TCP,STM32F103]
comments: true
author: admin
---
# STM32F1 ESP8266 TCP透传程序

## 简介

本仓库提供了一个基于STM32F103和ESP8266的TCP透传程序。通过该程序，您可以实现STM32F103与ESP8266之间的TCP透传功能。程序中还集成了SmartConfig功能，用户可以通过按键2实现WiFi配置，也可以通过程序直接写入路由器信息。

## 功能特点

- **TCP透传**：STM32F103与ESP8266之间实现TCP透传，方便数据传输。
- **SmartConfig**：通过按键2可以实现SmartConfig功能，方便用户配置WiFi信息。
- **路由器信息写入**：除了SmartConfig，用户还可以通过程序直接写入路由器信息，简化配置流程。

## 使用说明

1. **硬件连接**：
   - 将STM32F103与ESP8266按照电路图连接。
   - 确保按键2连接正确，用于触发SmartConfig功能。

2. **软件配置**：
   - 下载本仓库的代码到STM32F103开发板。
   - 根据需要配置路由器信息或使用SmartConfig功能。

3. **运行程序**：
   - 上电后，程序会自动初始化并尝试连接WiFi。
   - 如果需要使用SmartConfig，按下按键2即可进入配置模式。

## 注意事项

- 确保ESP8266固件版本支持SmartConfig功能。
- 在写入路由器信息时，请确保输入的信息准确无误。

## 贡献

欢迎大家提出改进建议或提交PR，共同完善这个项目。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[STM32F1ESP8266TCP透传程序](https://pan.quark.cn/s/a868cc3a1d99)