---
layout: post
title: "ESP8266入门教程：AT模式下手机与ESP8266通信（AP模式）"
date:   2022-03-06
tags: [ESP8266,模块,模式,AP,手机]
comments: true
author: admin
---
# ESP8266入门教程：AT模式下手机与ESP8266通信（AP模式）

## 简介
本资源文件提供了关于ESP8266模块在AT模式下如何通过AP模式与手机进行通信的详细教程。ESP8266是一款低成本、高性能的Wi-Fi模块，广泛应用于物联网设备中。通过本教程，您将学习如何配置ESP8266模块，使其作为热点（AP模式），并实现手机与模块之间的通信。

## 主要内容
1. **ESP8266模块概述**  
   ESP8266模块支持多种工作模式，包括STA模式、AP模式和STA+AP模式。本教程主要介绍AP模式的使用。

2. **配置WiFi模式**  
   使用AT指令`AT+CWMODE=2`将ESP8266配置为AP模式。

3. **设置网络参数**  
   使用AT指令`AT+CWSAP="ESP8266","123456789",4,4`设置网络名称、密码、通道号和加密方式。

4. **重启模块**  
   使用AT指令`AT+RST`重启ESP8266模块，使配置生效。

5. **使能多连接**  
   使用AT指令`AT+CIPMUX=1`使能多连接模式，允许多个设备连接到ESP8266。

6. **设置端口号**  
   使用AT指令`AT+CIPSERVER=1,5050`设置服务器端口号，通常选择常用的端口号。

7. **手机与ESP8266通信**  
   通过手机连接到ESP8266的热点，并使用网络调试助手进行通信。手机发送的数据可以通过串口在PC上显示。

## 使用步骤
1. 将ESP8266模块连接到电脑，并使用串口工具发送AT指令。
2. 按照上述步骤配置ESP8266模块。
3. 手机连接到ESP8266的热点，并使用网络调试助手进行通信。
4. 通过串口工具查看ESP8266接收到的数据。

## 注意事项
- 确保ESP8266模块的固件版本支持AT指令。
- 配置过程中，每条AT指令发送后需等待模块返回“OK”确认。
- 手机与ESP8266通信时，确保手机和模块在同一网络中。

## 总结
通过本教程，您将掌握如何在AT模式下配置ESP8266模块，使其作为热点与手机进行通信。这为后续的物联网项目开发提供了基础。

## 下载链接

[ESP8266入门教程AT模式下手机与ESP8266通信AP模式](https://pan.quark.cn/s/6ce121790228)