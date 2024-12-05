---
layout: post
title: "STLINK烧录STM32程序步骤"
date:   2021-12-29
tags: [ST,LINK,烧录,Keil5,STM32]
comments: true
author: admin
---
# ST-LINK烧录STM32程序步骤

本文详细介绍了如何使用ST-LINK工具将程序烧录到STM32F103C8T6微控制器中。内容包括驱动安装、Keil5配置、接线及烧录过程。通过连接ST-LINK与STM32的相应引脚，并在Keil5中设置相应参数，最终实现程序的顺利烧录。

## 材料准备
- ST-LINK驱动安装包
- STM32F103C8T6微控制器
- ST-LINK调试器
- 杜邦线
- Keil5开发环境

## 驱动安装
1. 下载ST-LINK驱动安装包。
2. 按照安装包内的详细教程进行驱动安装。

## Keil5配置
1. 打开Keil5，点击魔术棒进入配置界面。
2. 在“Debug”选项中选择ST-LINK调试器，并点击“Settings”进行进一步配置。
3. 在“Flash Download”选项中，确保已勾选“Reset and Run”选项，以便烧录完成后自动运行程序。
4. 依次点击“确定”和“OK”完成配置。

## 接线
按照以下方式连接ST-LINK与STM32：
- VCC(3.3V) <----------------> VCC
- GND <---------------------> GND
- SWIO <--------------------> SWDIO
- SWCLK <-------------------> SWCLK

接好后将ST-LINK插入电脑。

## 烧录步骤
1. 在Keil5中，依次点击“Build”和“Download”按钮。
2. 观察下方进度条，当进度条显示烧录成功后，即可完成烧录。

通过以上步骤，您可以顺利地将程序烧录到STM32F103C8T6微控制器中。

## 下载链接

[ST-LINK烧录STM32程序步骤分享](https://pan.quark.cn/s/9ad5f016a523)