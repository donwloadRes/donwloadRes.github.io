---
layout: post
title: "STM32程序ST-LINK下载指南"
date:   2021-05-08
tags: [下载,ST,LINK,STLINK,STM32]
comments: true
author: admin
---
# STM32程序ST-LINK下载指南

本资源文件提供了关于如何使用ST-LINK下载器下载STM32程序的详细指南。通过本指南，您将了解如何正确接线、配置软件以及进行程序下载。

## 内容概述

1. **软件下载**：提供了必要的软件下载链接和提取码。
2. **交流学习**：鼓励用户在安装过程中如有疑问，可以通过留言或私聊进行交流。
3. **相关链接**：提供了ST-LINK驱动安装和MDK5下载与安装的相关链接。
4. **常用单片机系统板**：介绍了常用的STM32F103C8T6系统板。
5. **STLINK下载器**：展示了STLINK下载器的图片。
6. **STM32程序STLINK下载流程**：
   - **接线**：详细说明了STLINK模块与系统板的接线方式。
   - **配置软件并下载**：指导用户如何使用MDK5打开并编译程序，配置ST-Link Debugger，并进行程序下载。
7. **注意事项**：提醒用户注意ST-LINK的供电能力有限，开发板需要外接电源。

## 使用步骤

1. **接线**：
   - 将STLINK模块的3.3V与系统板的3.3V连接。
   - 将STLINK模块的SWCLK与系统板的CLK(DCL)连接。
   - 将STLINK模块的SWDIO与系统板的DIO(IO)连接。
   - 建议同时使用Micro USB线供电。

2. **配置软件并下载**：
   - 使用MDK5打开需要下载的程序并编译。
   - 点击魔法棒，选择Debug选项，选择ST-Link Debugger。
   - 点击Settings，在Debug界面选择SW，Max设置为1.8M。
   - 在Flash Download界面，勾选Rest and Run，最后点击确定退出。
   - 点击下载按键Download（LOAD）进行程序下载。

## 注意事项

- ST-LINK主要用于下载与仿真，供电能力不强，开发板需要外接电源。

通过本指南，您将能够顺利完成STM32程序的ST-LINK下载，并解决可能遇到的问题。

## 下载链接

[STM32程序ST-LINK下载指南](https://pan.quark.cn/s/9eeaba4d5659)