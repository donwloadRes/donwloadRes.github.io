---
layout: post
title: "STM32F103 TIM3通道1(PA6) PWM输入捕获方波程序"
date:   2023-08-28
tags: [PWM,捕获,TIM3,STM32,占空比]
comments: true
author: admin
---
# STM32F103 TIM3通道1(PA6) PWM输入捕获方波程序

## 项目简介

本项目针对STM32F103系列微控制器，实现了利用TIM3的通道1（引脚PA6）进行PWM信号的输入捕获功能。该功能对于需要分析外部PWM信号频率和占空比的应用场景极为有用。通过配置STM32的定时器TIM3，我们能够精确测量并解析接收到的PWM信号特性。捕获到的波形数据随后通过USART1发送出去，允许用户在计算机或者其他串口设备上监控波形的频率和占空比，便于实时数据分析和调试。

## 技术要点

- **TIM3配置**：详细配置TIM3作为输入捕获模式，指定PA6为捕获引脚。
- **PWM输入捕获**：设置TIM3以准确捕获外部PWM信号的上升沿或下降沿，实现对波形周期的测量。
- **频率与占空比计算**：根据捕获到的周期时间和高电平时间，动态计算并处理PWM信号的频率和占空比。
- **USART通讯**：利用USART1接口将计算得到的频率和占空比数据发送至电脑或其他串行设备显示，采用标准的串行通信协议。

## 使用指南

1. **环境准备**：
   - IDE推荐使用Keil MDK或STM32CubeIDE等支持STM32开发的工具。
   - 确保已安装对应的STM32库或者HAL库。
   
2. **硬件连接**：
   - 将外部PWM信号源连接到STM32开发板的PA6引脚。
   - 使用串口线连接STM32的USART1（通常是TX管脚）到电脑的串口，用于接收数据。

3. **编译与烧录**：
   - 打开项目工程，编译无误后，将程序烧录至STM32F103芯片中。

4. **数据监视**：
   - 在电脑端打开串口助手，配置相应的波特率（例如9600或115200），观察频率和占空比数据输出。

## 注意事项

- 根据你的具体需求调整USART的波特率和其他配置参数。
- 确保外部PWM信号的电压水平与STM32逻辑电平相匹配。
- 在进行应用前，请确保理解TIM3的输入捕获原理和USART通信机制。

## 开发与贡献

该项目面向所有开发者开放，欢迎fork和提出改进意见。如果你发现了任何bug或者有新的功能建议，请通过提交Issue的方式联系我们。共同合作，让代码更加完善！

---

此项目的分享旨在促进STM32学习者和技术爱好者之间的交流，为嵌入式系统的开发提供实用参考案例。希望对你有所帮助！

## 下载链接

[STM32F103TIM3通道1PA6PWM输入捕获方波程序](https://pan.quark.cn/s/47717c6a61a8)