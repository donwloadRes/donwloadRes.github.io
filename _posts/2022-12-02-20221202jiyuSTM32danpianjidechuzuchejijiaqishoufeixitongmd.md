---
layout: post
title: "基于STM32单片机的出租车计价器收费系统"
date:   2023-08-14
tags: [计费,出租车,STM32,单片机,仿真]
comments: true
author: admin
---
# 基于STM32单片机的出租车计价器收费系统

## 项目简介

本项目是一个基于STM32单片机的出租车计价器收费系统，包含Proteus仿真和程序源码。该系统通过STM32单片机控制，实现了出租车的计费功能，并能够在LCD1602显示屏上显示出租车的温湿度、行驶里程和计费总价。

## 功能特点

1. **计费功能**：系统支持起步价和按公里数计费，通过按键进行设置开始计费和计费清零。
2. **温湿度显示**：使用DHT11温湿度传感器，实时显示出租车的温湿度信息。
3. **行驶里程显示**：通过L298N驱动电机转动，模拟出租车启动，计费系统开始计费，并显示行驶里程。
4. **LCD1602显示**：使用LCD1602显示屏，显示出租车的温湿度、行驶里程和计费总价。

## 仿真演示

本项目使用Proteus软件进行仿真，演示视频和程序源码均包含在资源文件中。仿真演示视频展示了系统的运行过程，程序源码部分有详细的中文注释，方便新手理解和学习。

## 设计软件

本设计使用C语言编程设计，程序代码采用Keil5编写，程序有中文注释，新手容易看懂。仿真采用Proteus软件进行仿真，演示视频使用的是Proteus8.9版本。

## 程序打开方法

特别注意：下载资料包以后一定要先解压（建议解压到桌面上，文件路径太深会导致程序打开异常），解压后再用Keil5打开。

## 资料清单

资源文件中包含以下内容：
- 程序源码
- Proteus仿真文件
- 仿真演示视频
- 相关软件包

## 适用对象

本项目适用于学习STM32单片机、嵌入式系统开发、出租车计价器设计的同学和开发者。通过本项目的学习和实践，可以深入理解STM32单片机的应用和出租车计价器的工作原理。

## 联系我们

如有任何问题或建议，欢迎通过CSDN博客联系作者。

## 下载链接

[基于STM32单片机的出租车计价器收费系统](https://pan.quark.cn/s/90405cb98a10)