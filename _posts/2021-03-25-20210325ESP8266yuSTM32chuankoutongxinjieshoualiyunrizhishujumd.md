---
layout: post
title: "ESP8266与STM32串口通信接收阿里云日志数据"
date:   2021-10-20
tags: [STM32,ESP8266,OLED,串口,日志]
comments: true
author: admin
---
# ESP8266与STM32串口通信接收阿里云日志数据

## 简介
本项目展示了如何使用ESP8266开发板NodeMCU与STM32最小系统进行串口通信，并通过该通信方式接收阿里云日志数据。通过本项目，您可以学习到如何将物联网设备与云平台进行数据交互，并实现数据的本地处理与显示。

## 硬件需求
1. NodeMCU型号：ESP8266MOD
2. STM32型号：STM32最小系统
3. OLED显示屏

## 软件需求
1. Arduino IDE（需包含esp8266 by ESP8266和PubSubClient库）
2. Keil uVision5

## 引脚连接
1. ESP8266-NODE与STM32连线：
   - ESP8266-NODE RX -> STM32 A9
   - ESP8266-NODE TX -> STM32 A10
2. STM32与OLED连线：
   - STM32 B8 -> OLED SCL
   - STM32 B9 -> OLED SDA
   - STM32 VCC -> OLED VCC
   - STM32 GND -> OLED GND

## 代码说明
### ESP8266-NODE代码（Arduino IDE）
- 使用WiFi和MQTT协议连接到阿里云服务器。
- 通过回调函数处理接收到的日志数据，并通过串口发送给STM32。

### STM32代码（Keil uVision5）
- 初始化串口和OLED显示屏。
- 接收来自ESP8266的日志数据，并在OLED上显示。

## 使用步骤
1. 在Arduino IDE中编写并上传ESP8266的代码。
2. 在Keil uVision5中编写并上传STM32的代码。
3. 连接硬件并上电，确保ESP8266成功连接到WiFi和阿里云服务器。
4. STM32将通过串口接收并显示阿里云日志数据。

## 注意事项
- 确保WiFi和MQTT服务器的配置正确。
- 检查硬件连接是否正确，避免短路或接触不良。

通过本项目，您可以深入了解物联网设备与云平台的通信机制，并掌握如何在嵌入式系统中处理和显示云端数据。

## 下载链接

[ESP8266与STM32串口通信接收阿里云日志数据](https://pan.quark.cn/s/fb002fb11dab)