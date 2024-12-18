---
layout: post
title: "基于STM32F103R6的双机通信Protues仿真"
date:   2020-03-20
tags: [单片机,仿真,Proteus,串口,STM32F103R6]
comments: true
author: admin
---
# 基于STM32F103R6的双机通信Protues仿真

## 项目描述

本项目提供了一个基于STM32F103R6微控制器的双机通信仿真资源文件。通过Proteus仿真平台，实现了单片机A与单片机B之间的串口通信，并结合LED灯和LCD显示屏进行数据交互和显示。

## 功能描述

1. **系统运行指示**：
   - 在程序运行过程中，单片机A的LED1灯以500ms的周期进行闪烁，提示系统正在运行。

2. **LED控制**：
   - 单片机A通过串口向单片机B发送字符‘1’，单片机B收到数据后控制LED2灯点亮。
   - 单片机A通过串口向单片机B发送字符‘2’，单片机B收到数据后控制LED2灯熄灭。

3. **按键输入与学号显示**：
   - 单片机A连接一个按键，按下按键后，单片机A通过串口向单片机B发送数据“学号”。
   - 单片机B收到正确的“学号”时，LCD显示屏将显示该学号。

## 软件环境

- **MDK KEIL**：用于编写和编译STM32F103R6的固件代码。
- **Proteus 8 Professional**：用于仿真整个系统的硬件电路和软件逻辑。

## 使用说明

1. **仿真环境搭建**：
   - 使用Proteus 8 Professional打开仿真文件，确保所有元件和连接正确无误。
   - 在MDK KEIL中编译并生成HEX文件，将其加载到Proteus中的STM32F103R6微控制器中。

2. **运行仿真**：
   - 启动Proteus仿真，观察LED1灯的闪烁情况，确认系统正在运行。
   - 通过按键输入学号，观察LCD显示屏是否正确显示学号。

3. **调试与修改**：
   - 根据实际需求，可以在MDK KEIL中修改代码，重新编译并加载到Proteus中进行测试。

## 注意事项

- 确保Proteus和MDK KEIL的版本兼容，避免仿真过程中出现不可预知的问题。
- 在仿真过程中，注意观察串口通信的数据传输情况，确保数据发送和接收的准确性。

## 贡献与反馈

欢迎对本项目提出改进建议或反馈问题。您可以通过提交Issue或Pull Request的方式参与项目的改进。

## 下载链接

[基于STM32F103R6的双机通信Protues仿真](https://pan.quark.cn/s/be8178239abf)