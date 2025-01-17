---
layout: post
title: "TEC控制器 ADN8835中文参考手册"
date:   2022-11-16
tags: [ADN8835,温度,电压,TEC,温度控制]
comments: true
author: admin
---
# TEC控制器 ADN8835中文参考手册

## 资源描述

ADN8835是一款高集成度的单芯片TEC控制器。它包括线性电压调节模块（power stage）、脉冲宽度调制(PWM) 电压调节模块和两个零漂移、轨到轨斩波放大器。线性控制器和PWM驱动器用于控制H桥配置中的内部功率MOSFET。通过测量热传感器反馈电压，并使用集成的运算放大器作为比例-积分-微分(PID)补偿器来调理信号，ADN8835通过TEC驱动电流，将连接至TEC模块的激光二极管或无源组件的温度稳定到编程的目标温度。

ADN8835支持负温度系数(NTC)热敏电阻以及正温度系数(PTC)电阻温度检测器(RTD)。目标温度采用模拟电压的形式设置，其可来源于数模转换器(DAC)或外部电阻分压器。ADN8835温度控制环路利用内置零漂移斩波放大器通过PID补偿方式实现稳定。内部2.50 V基准电压具备1%的精确输出能力，提供热敏电阻温度检测电桥和分压器网络偏置，从而在加热和冷却模式下对最大TEC电流和电压限值进行编程。它利用零漂移斩波放大器，通过自主模拟温度控制环路可维持出色的长期温度稳定性。

## 适用范围

- 激光二极管温度控制
- 无源组件温度稳定
- 需要高精度温度控制的系统

## 主要特点

- 高集成度单芯片设计
- 线性电压调节模块和PWM电压调节模块
- 零漂移、轨到轨斩波放大器
- 支持NTC和PTC温度检测
- 内置2.50 V基准电压，精度1%
- 自主模拟温度控制环路

## 使用说明

1. **温度设定**：通过外部DAC或电阻分压器设置目标温度。
2. **温度反馈**：使用NTC或PTC热敏电阻进行温度检测。
3. **PID补偿**：利用内置运算放大器进行PID补偿，实现温度稳定。
4. **电流和电压限制**：通过内部基准电压和外部电阻网络设置最大TEC电流和电压限值。

## 注意事项

- 确保热敏电阻的连接正确，以避免温度检测误差。
- 在设置目标温度时，考虑系统的响应时间和稳定性。
- 定期校准基准电压，以确保温度控制的精度。

## 文件下载

请点击下方链接下载ADN8835中文参考手册：

[下载ADN8835中文参考手册](./ADN8835_Chinese_Manual.pdf)

## 下载链接

[TEC控制器ADN8835中文参考手册分享](https://pan.quark.cn/s/deba227919ff)