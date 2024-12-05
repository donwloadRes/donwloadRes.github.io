---
layout: post
title: "TJA1145配置休眠唤醒"
date:   2022-03-11
tags: [唤醒,TJA1145,休眠,使能,配置]
comments: true
author: admin
---
# TJA1145配置休眠唤醒

## 简介
本资源文件详细介绍了如何配置TJA1145模块的休眠唤醒功能。TJA1145是一款高速CAN收发器，广泛应用于汽车电子系统中。通过配置TJA1145的休眠唤醒功能，可以有效降低系统的功耗，延长电池寿命。

## 内容概述
1. **基础知识**
   - CAN总线通常采用双绞线来传输差分信号。
   - CAN收发器的作用是将CAN总线上的差分信号转换为高电平（逻辑1）和低电平（逻辑0）的数字信号。
   - 差分信号传输的优势在于其抗干扰能力强。

2. **TJA1145引脚说明**
   - INH：唤醒输出引脚，用于控制开关电源芯片使能。
   - SDO、SDI、SCK、SCSN：通过SPI读写TJA1145寄存器。
   - WAKE：唤醒输入引脚，可配置唤醒信号边沿（上升沿、下降沿）。

3. **SPI链路验证**
   - TJA1145通过SPI通信来配置相关寄存器，首先需要保证MCU和TJA1145之间的通信正常。
   - 通过读取设备ID来验证SPI通信是否正常。

4. **休眠唤醒说明**
   - 唤醒方式包括KL15唤醒和CAN唤醒。
   - KL15唤醒：指钥匙点火（ACC）信号，输入高时给MCU供电。
   - CAN唤醒：检测到唤醒报文时，INH引脚拉高，使能电源芯片给MCU供电。

5. **休眠唤醒配置**
   - 启用Partial Networking。
   - 使能CAN选择性唤醒。
   - 设置数据速率为500k。
   - 配置帧控制寄存器，识别格式为标准帧。
   - 使能CAN唤醒检测，使能唤醒pin脚上升沿检测。
   - 清除所有事件状态位。

6. **唤醒报文设置**
   - TJA1145只能标准帧唤醒，设置唤醒ID为0x7A4。

7. **实现代码**
   - 提供了读写寄存器的函数代码示例。
   - 初始化函数和休眠函数的代码示例。

## 使用方法
1. 下载资源文件并解压。
2. 根据README.md中的说明，配置TJA1145模块。
3. 参考代码示例，实现MCU与TJA1145的通信和休眠唤醒功能。

## 注意事项
- TJA1145设计为只支持特定CAN报文唤醒，不支持CANFD唤醒，以防止仅在CAN通信时产生总线错误。
- 在切换到睡眠模式前，必须至少启用一个常规唤醒事件，并清除所有事件状态位。

通过本资源文件，您可以轻松配置TJA1145模块的休眠唤醒功能，实现低功耗设计。

## 下载链接

[TJA1145配置休眠唤醒](https://pan.quark.cn/s/70ce2b9a1682)