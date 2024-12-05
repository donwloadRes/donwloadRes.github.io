---
layout: post
title: "STM32低功耗三种方式唤醒"
date:   2023-05-26
tags: [RTC,停机,唤醒,中断,系统]
comments: true
author: admin
---
# STM32低功耗三种方式唤醒

## 项目描述

本项目提供了一个关于STM32低功耗唤醒的资源文件，详细介绍了如何通过三种方式唤醒STM32系统。项目设计要求系统在启动2秒后进入停机模式，并通过RTC报警事件或外部按键中断来唤醒系统。唤醒后，系统会重新配置时钟并进入下一个停机周期，实现低功耗循环。

## 设计要求

1. **系统进入和退出睡眠模式**：
   - 系统启动2秒后，配置RTC在3秒钟后产生报警事件。
   - 通过WFI指令使系统进入停机模式。
   - 系统可以通过按下Key按钮或RTC报警中断唤醒。
   - 唤醒后，系统时钟恢复到停机前的状态。
   - 经过一段延时后，系统再次进入停机状态，循环往复。

2. **硬件电路设计**：
   - 硬件电路与7.1小节应用实例相同，具体可见图7-10。
   - Key按钮用于通过PB9产生外部中断。
   - LED1、LED2、LED3、LED4用于显示处理器模式和中断触发情况。

3. **软件程序设计**：
   - 主要程序内容包括：配置GPIOB口、RTC、外部中断；配置PB9引脚为外部中断，下降沿触发；配置RTC报警中断，上升沿触发。
   - 中断服务子程序内容：切换LED2和LED3灯的状态。
   - 工程包含3个源文件：STM32F10x.s、stm32f10x_it.c和main.c。

## 主要函数介绍

- **SYSCLKConfig_STOP**：处理器从停机模式唤醒后，配置系统时钟、使能HSE和PLL，并以PLL作为系统时钟源。
- **GPIO_Configuration**：配置GPIO的PC6、PC7、PC8、PC9和PB9。
- **EXTI_Configuration**：配置外部中断线9（PB9）和17（RTC报警）。
- **NVIC_Configuration**：配置NVIC及中断向量表，主要配置外部中断线9和17。
- **EXTI9_5_IRQHandler**：处理按钮Key（PB9）触发的中断，翻转LED2灯的状态。
- **RTCAlarm_IRQHandler**：处理RTC报警触发的中断，翻转LED3灯的状态，并清除唤醒标志。

## 运行过程

1. **软件调试模式**：
   - 使用Keil uVision3通过ULINK 2仿真器连接EduKit-M3实验平台，打开PWR_TEST子目录下的PWR.Uv2例程，编译链接工程。
   - 选择软件调试模式，点击Debug菜单，选择Start/Stop Debug Session项或Ctrl+F5键，在逻辑分析仪中添加GPIOC_ODR.6、GPIOC_ODR.7、GPIOC_ODR.8、GPIOC_ODR.9，点击Run按钮即可观察LED灯的变化。

2. **硬件调试模式**：
   - 选择硬件调试模式，下载程序并运行，观察LED灯的变化情况。
   - 注意：系统进入停机模式后，无法使用仿真器进行调试。

3. **下载程序**：
   - 退出Debug模式，打开Flash菜单>Download，将程序下载到EduKit-M3实验平台的Flash中，按RESET键复位，观察LED灯的情况。
   - 正常情况下，系统处于运行模式时LED1亮、LED4灭；系统处于停机状态时LED1灭、LED4亮；按下KEY按钮时LED2灯状态反转；发生RTC报警时LED3状态反转。

## 注意事项

- 系统进入停机模式后，无法使用仿真器进行调试。
- 下载程序到实验平台后，按RESET键复位，观察LED灯的变化情况。

## 下载链接

[STM32低功耗三种方式唤醒](https://pan.quark.cn/s/1700d8a3b6e2)