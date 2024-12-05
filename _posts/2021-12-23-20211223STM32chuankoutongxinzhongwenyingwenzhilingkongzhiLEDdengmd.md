---
layout: post
title: "STM32串口通信：中文英文指令控制LED灯"
date:   2023-09-15
tags: [串口,单片机,指令,STM32,绿灯]
comments: true
author: admin
---
# STM32串口通信：中文英文指令控制LED灯

## 项目概述

本项目实现了一种通过串口助手利用中英文混合指令远程控制STM32单片机上LED灯的功能。基于入门级微控制器STM32F103C8T6，此示例展示了如何在嵌入式系统中集成简单的人机交互界面，尤其是展示如何接收并解析包含中文的串口命令。适合初学者学习了解STM32的串口通讯和HAL库的使用。

## 功能描述

- **发送“打开绿灯”**：单片机会接收到指令，并回复“绿灯已打开”，同时点亮绿灯。
- **发送“关闭绿灯”**：单片机反馈“绿灯已关闭”，并熄灭绿灯。
- **发送`open_Red`**：单片机将响应“open_Red_Yes”，开启红灯。
- **发送`close_Red`**：单片机返回“close_Red_Yes”，关闭红灯。

## 技术栈

- **主控芯片**：STM32F103C8T6
- **开发环境**：STM32CubeMX配置 + Keil MDK V5
- **库函数**：HAL库
- **通讯方式**：UART（通用异步收发传输器）

## 特点

- 全面的代码注释，便于新手理解。
- 中文指令支持，增加人机交互的友好性。
- 简洁明了地演示了串口通信的基本流程和错误处理逻辑。
- 适用于学习STM32基础、串口编程以及HAL库应用的学习者。

## 使用指南

1. **环境搭建**：首先使用STM32CubeMX配置好STM32F103C8T6的相关外设，特别是USART设置，并生成Keil项目。
2. **编码**：在Keil中查看和理解已提供的代码，特别是串口中断服务程序部分，如何根据接收到的数据执行相应操作。
3. **测试**：连接好硬件，打开串口助手，通过USB线与PC通信。输入上述指定指令进行测试。
4. **反馈处理**：观察单片机的LED灯状态变化及串口助手上的反馈信息，确保一切按预期工作。

## 注意事项

- 确保你的电脑串口助手设置与单片机的波特率一致。
- 调试过程中，如果遇到问题，检查串口线路连接是否正确以及电源供应。
- 欢迎对代码中的任何不解之处留言提问，共同探讨学习。

此项目不仅是一个实用的技术实践，也是探索非传统英文指令在物联网设备控制中的可能性，开启了使用中文指令进行电子设备控制的新途径。

## 下载链接

[STM32串口通信中文英文指令控制LED灯](https://pan.quark.cn/s/c966b92c0a2b)