---
layout: post
title: "STM32ESP8266连接onenet上传温湿度数据远程控制LEDMQTT"
date:   2024-11-24
tags: [STM32,OneNet,ESP8266,温湿度,LED]
comments: true
author: admin
---
# STM32+ESP8266连接onenet上传温湿度数据+远程控制LED（MQTT）

## 项目简介

本项目提供了一个基于STM32和ESP8266的物联网应用示例，通过MQTT协议将温湿度数据上传至OneNet云平台，并实现远程控制LED的功能。项目资源文件包含完整的代码和配置文件，方便开发者快速上手和集成到自己的项目中。

## 主要功能

1. **温湿度数据采集**：使用STM32内置的传感器或外接传感器采集环境温湿度数据。
2. **数据上传至OneNet**：通过ESP8266模块连接到Wi-Fi网络，使用MQTT协议将采集到的温湿度数据上传至OneNet云平台。
3. **远程控制LED**：通过OneNet平台发送控制指令，实现远程控制STM32板载LED的开关状态。

## 文件结构

- `stm32_code/`：包含STM32的固件代码，负责温湿度数据的采集和LED控制。
- `esp8266_code/`：包含ESP8266的固件代码，负责与OneNet平台的MQTT通信。
- `onenet_config/`：包含OneNet平台的配置文件和MQTT连接参数。
- `README.md`：本文件，提供项目的基本介绍和使用说明。

## 使用说明

1. **硬件准备**：
   - STM32开发板（如STM32F103C8T6）
   - ESP8266模块（如ESP-01）
   - 温湿度传感器（可选，如DHT11）
   - LED和电阻（用于远程控制）

2. **软件准备**：
   - Keil uVision（用于编译STM32代码）
   - Arduino IDE（用于编译ESP8266代码）
   - OneNet账号（用于创建MQTT设备和数据流）

3. **配置OneNet平台**：
   - 登录OneNet平台，创建一个新的设备和数据流，获取MQTT连接所需的API Key和设备ID。
   - 将获取到的参数填入`onenet_config/mqtt_config.h`文件中。

4. **编译和烧录**：
   - 使用Keil uVision打开`stm32_code/`目录下的工程文件，编译并烧录到STM32开发板。
   - 使用Arduino IDE打开`esp8266_code/`目录下的工程文件，编译并烧录到ESP8266模块。

5. **运行测试**：
   - 将STM32和ESP8266连接到同一Wi-Fi网络。
   - 启动STM32和ESP8266，观察OneNet平台上的数据上传情况。
   - 通过OneNet平台发送控制指令，测试LED的远程控制功能。

## 注意事项

- 请确保STM32和ESP8266的固件版本与本项目提供的代码兼容。
- 在配置OneNet平台时，请妥善保管API Key等敏感信息，避免泄露。
- 如果使用外接温湿度传感器，请根据传感器型号调整STM32代码中的初始化参数。

## 贡献与反馈

欢迎开发者对本项目进行改进和优化，如果您有任何问题或建议，请在GitHub仓库中提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅`LICENSE`文件。

## 下载链接

[STM32ESP8266连接onenet上传温湿度数据远程控制LEDMQTT](https://pan.quark.cn/s/df61fcd8442f)