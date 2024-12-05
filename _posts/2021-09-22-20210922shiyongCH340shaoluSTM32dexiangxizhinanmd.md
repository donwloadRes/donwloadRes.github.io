---
layout: post
title: "使用CH340烧录STM32的详细指南"
date:   2022-12-26
tags: [CH340,引脚,烧录,STM32,连接]
comments: true
author: admin
---
# 使用CH340烧录STM32的详细指南

本文详细介绍了如何使用CH340 USB转TTL模块将STM32F103C8T6进入下载模式，并通过FlyMcu软件进行固件烧录的步骤。以下是具体操作流程：

## 准备工作

1. **硬件准备**：
   - STM32F103C8T6最小系统板
   - CH340 USB转TTL下载器
   - 杜邦线若干
   - 电脑（已安装CH340驱动）

2. **软件准备**：
   - FlyMcu软件（可在网上下载）

## 操作步骤

### 1. 硬件连接

1. 将CH340 USB转TTL模块连接到计算机的USB接口上。
2. 使用杜邦线将CH340模块的TXD引脚连接到STM32的RX引脚，将CH340模块的RXD引脚连接到STM32的TX引脚。
3. 将CH340模块的GND引脚连接到STM32的GND引脚。
4. 将STM32的BOOT0引脚连接到VCC（高电平），将BOOT1引脚连接到GND（低电平），以进入下载模式。

### 2. 软件设置

1. 打开FlyMcu软件。
2. 在软件中搜索串口，找到CH340对应的串口。
3. 选择搜索到的串口，波特率一般默认为115200。
4. 点击“...”按钮，选择要下载的HEX文件。
5. 勾选“编程后执行”选项。
6. 选择“不使用RTS和DTR”。

### 3. 开始烧录

1. 点击“开始编程”按钮，开始连接后，按下STM32的复位键。
2. 按下复位键之后，烧录过程将自动开始。

### 4. 烧录成功后的操作

1. 烧录成功后，记得将BOOT0引脚的短接帽复原（连接到GND），以确保程序正常运行。

## 注意事项

- 确保CH340驱动已正确安装。
- 烧录过程中，确保BOOT0和BOOT1的电平设置正确。
- 烧录成功后，务必恢复BOOT0的短接帽，否则程序无法正常运行。

通过以上步骤，您可以成功使用CH340模块烧录STM32F103C8T6的固件。

## 下载链接

[使用CH340烧录STM32的详细指南](https://pan.quark.cn/s/7143ba45db8e)