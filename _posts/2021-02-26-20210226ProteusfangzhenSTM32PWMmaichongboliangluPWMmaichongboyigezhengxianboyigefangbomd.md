---
layout: post
title: "Proteus仿真--STM32 PWM脉冲波（两路PWM脉冲波，一个正弦波一个方波）"
date:   2023-08-22
tags: [PWM,脉冲,Proteus,方波,仿真]
comments: true
author: admin
---
# Proteus仿真--STM32 PWM脉冲波（两路PWM脉冲波，一个正弦波一个方波）

## 作品描述

本资源提供了一个基于Proteus仿真平台的STM32 PWM脉冲波生成项目。该项目通过STM32F103微控制器生成两路PWM脉冲波，其中一路经过RC滤波电路后产生正弦波，另一路直接输出方波。方波的频率为125赫兹，周期为8毫秒，占空比为20%；正弦波的频率为50赫兹，周期为20毫秒。

## 使用材料

- STM32F103微控制器
- RC滤波电路

## 平台

- Proteus仿真软件
- Keil开发平台

## 技术实现

1. **PWM脉冲波生成**：STM32微控制器通过定时器生成两路PWM脉冲波。
2. **RC滤波电路**：其中一路PWM信号经过RC滤波电路后，转换为正弦波。
3. **方波输出**：另一路PWM信号直接输出为方波。

## 资源内容

- Proteus仿真电路图一份
- Keil平台的STM32程序

## 使用方法

1. 在Proteus中打开仿真电路图。
2. 点击STM32器件，选择Program File选项。
3. 选择Keil生成的hex文件路径。
4. 点击运行，即可观察到仿真效果。

## 适用人群

本资源适用于需要使用Proteus仿真PWM脉冲波（两路PWM脉冲波，一个正弦波一个方波）的开发者或学习者。

## 下载链接

[Proteus仿真--STM32PWM脉冲波两路PWM脉冲波一个正弦波一个方波](https://pan.quark.cn/s/933519626055)