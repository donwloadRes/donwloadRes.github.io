---
layout: post
title: "STM32 HAL库 ADC 温度传感器与 VREFINT 示例"
date:   2020-05-13
tags: [串口,VREFINT,Keil,MDK,温度传感器]
comments: true
author: admin
---
# STM32 HAL库 ADC 温度传感器与 VREFINT 示例

## 项目描述

本资源文件提供了一个基于STM32F103C8T6单片机的ADC示例程序，使用Keil MDK 5.32版本进行开发。该程序通过ADC1模块采集温度传感器和内部参考电压（VREFINT）的数据，并通过串口输出相关信息。

## 功能特点

- **硬件平台**：STM32F103C8T6单片机
- **开发环境**：Keil MDK 5.32
- **主要功能**：
  - 使用ADC1模块采集温度传感器数据
  - 采集内部参考电压（VREFINT）数据
  - 通过串口输出采集到的温度和VREFINT数据

## 使用说明

1. **硬件准备**：
   - 准备一块STM32F103C8T6开发板
   - 连接串口调试工具（如USB转TTL模块）以便查看串口输出信息

2. **软件准备**：
   - 安装Keil MDK 5.32或更高版本
   - 下载本资源文件中的代码并导入到Keil MDK中

3. **编译与下载**：
   - 在Keil MDK中编译代码
   - 将编译后的程序下载到STM32F103C8T6开发板

4. **串口查看**：
   - 打开串口调试工具，设置波特率与代码中一致（通常为9600）
   - 查看串口输出信息，获取温度和VREFINT数据

## 注意事项

- 确保硬件连接正确，特别是串口连接部分
- 代码中的串口波特率设置需与串口调试工具一致
- 如有需要，可根据实际情况调整ADC采样周期和滤波参数

## 贡献与反馈

如果您在使用过程中遇到问题或有改进建议，欢迎通过GitHub Issues或Pull Requests进行反馈和贡献。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[STM32HAL库ADC温度传感器与VREFINT示例](https://pan.quark.cn/s/c5f3d453b215)