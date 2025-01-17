---
layout: post
title: "基于STM32F103单片机的地震震动开关检测报警器系统"
date:   2020-02-13
tags: [震动,阈值,设置,频率,检测]
comments: true
author: admin
---
# 基于STM32F103单片机的地震震动开关检测报警器系统

## 项目简介

本项目基于STM32F103单片机，设计并实现了一个地震震动开关检测报警器系统。该系统能够实时检测地震震动频率，并通过LCD1602液晶显示屏显示震动频率，同时根据设定的震动阈值触发蜂鸣器报警。

## 系统功能

1. **震动频率检测**：通过震动传感器实时检测地震震动频率，并将频率显示在LCD1602液晶显示屏上。
2. **震动频率采集**：系统通过单位时间内检测震动传感器的震动次数来获取震动频率。
3. **震动阈值设置**：系统提供三个按键用于设置震动阈值，分别为设置键、设置+、设置-。设置+和设置-只有在设置模式下才能进行操作。
4. **报警功能**：当检测到的震动频率超过设定的阈值时，系统会触发蜂鸣器报警。
5. **灵敏度调节**：震动传感器上的电位器可以调节检测的灵敏度。

## 硬件组成

- **STM32F103C8T6单片机核心板**：作为系统的核心控制器。
- **震动传感器**：用于检测地震震动频率。
- **LCD1602液晶显示屏**：用于实时显示震动频率。
- **蜂鸣器**：用于报警。
- **按键控制**：用于设置震动阈值。
- **电源**：为系统提供电力支持。

## 使用说明

1. **系统启动**：接通电源后，系统自动启动并开始检测震动频率。
2. **频率显示**：震动频率会实时显示在LCD1602液晶显示屏上。
3. **阈值设置**：通过按键设置震动阈值，设置完成后，系统会根据设定的阈值进行报警判断。
4. **报警触发**：当震动频率超过设定的阈值时，蜂鸣器会发出报警声。

## 注意事项

- 请确保震动传感器安装稳固，以保证检测的准确性。
- 在设置震动阈值时，请根据实际需求进行合理设置。
- 系统掉电后，设置的阈值不会丢失，系统会自动恢复上次设置的阈值。

## 项目文件

本仓库提供了完整的项目文件，包括源代码、原理图和PCB设计文件。用户可以根据需要进行下载和使用。

## 贡献

欢迎对本项目进行改进和优化，如果您有任何建议或改进意见，请提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[基于STM32F103单片机的地震震动开关检测报警器系统](https://pan.quark.cn/s/ccb1d90bd687)