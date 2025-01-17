---
layout: post
title: "STM32 ADC采集正弦波并使用DSP库FFT计算失真度"
date:   2023-03-22
tags: [STM32,ADC,FFT,失真度,采集]
comments: true
author: admin
---
# STM32 ADC采集正弦波并使用DSP库FFT计算失真度

## 项目描述

本项目基于正点原子STM32F103 Mini板，使用Keil5作为开发平台，实现了通过STM32自带的ADC模块采集外部输入的正弦信号，并利用STM32官方DSP库中的FFT算法对采集到的数据进行处理，最终计算出正弦波的失真度。

## 主要功能

1. **ADC采集**：使用STM32自带的ADC模块采集外部输入的正弦信号。由于STM32的ADC采集范围为0~3.3V，因此外部输入的信号需要进行偏置处理。

2. **FFT处理**：采用STM32官方DSP库中的FFT算法对采集到的数据进行处理，支持64、256、1024点的FFT处理。

3. **失真度计算**：通过对FFT处理后的数据进行分析，计算出正弦波的失真度。

4. **采样频率配置**：采样频率可根据实际需求进行自由配置，只需修改相关参数即可。

## 兼容性

本项目基于正点原子STM32F103 Mini板开发，但其他类型的STM32芯片只需修改相关配置即可兼容。

## 使用说明

1. **硬件连接**：将外部正弦信号源连接到STM32的ADC输入引脚，并确保信号经过偏置处理，使其电压范围在0~3.3V之间。

2. **软件配置**：在Keil5中打开项目，根据实际使用的STM32型号修改相关配置（如时钟配置、ADC引脚配置等）。

3. **采样频率设置**：根据实际需求修改采样频率，具体参数可在代码中进行调整。

4. **编译与下载**：编译项目并下载到STM32开发板上，运行程序即可开始采集和处理数据。

5. **结果查看**：程序运行后，可以通过串口或其他方式查看计算出的正弦波失真度。

## 注意事项

- 外部输入的正弦信号需要进行偏置处理，以确保ADC采集的电压范围在0~3.3V之间。
- 采样频率的设置应根据实际需求进行调整，过高或过低的采样频率都可能影响数据的准确性。

## 参考资料

- STM32官方DSP库文档
- STM32F103 Mini板相关资料

## 联系我们

如有任何问题或建议，欢迎通过GitHub Issues或邮件联系我们。

## 下载链接

[STM32ADC采集正弦波并使用DSP库FFT计算失真度](https://pan.quark.cn/s/bf1d348f66cd)