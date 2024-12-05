---
layout: post
title: "STM32 STLINK Utility 使用指南"
date:   2024-09-19
tags: [STM32,ST,HEX,点击,LINK]
comments: true
author: admin
---
# STM32 ST-LINK Utility 使用指南

## 简介
STM32 ST-LINK Utility 是一款由意法半导体（STMicroelectronics）提供的软件工具，主要用于配合 ST-LINK 编程器/调试器硬件设备，以实现对 STM32 系列微控制器的编程和调试。该工具类似于 J-Link 工具对于 J-Link 编程器的作用，具有以下主要功能：

- **代码烧写**：可以直接下载 HEX 文件或 BIN 文件到 STM32 微控制器的闪存中。
- **代码加密**：可以对下载的代码进行读保护，防止未经授权的读取。
- **批量生产**：在产品批量生产阶段，可以快速高效地进行代码烧写。
- **数据读取**：可以快速读取 STM32 芯片的 FLASH 数据、芯片型号、ID、版本等信息。

## 下载与安装
### 下载
STM32 ST-LINK Utility 可以从意法半导体官方网站下载，也可以通过其他第三方资源站点获取。建议从官方渠道下载以确保软件的完整性和安全性。

### 安装
1. **解压软件**：双击下载的安装包，进入准备安装（解压）过程。
2. **进入安装向导**：点击“Next”。
3. **同意许可**：点击“Yes”。
4. **选择安装路径**：可以选择默认路径或自定义路径，点击“Next”。
5. **安装过程**：等待安装完成，通常不到一分钟时间。
6. **安装驱动**：安装最后会提示安装驱动，点击“下一步”，最后点击“完成”。
7. **完成安装**：点击“Finish”完成上位机软件及 ST-LINK 驱动的安装。

## 基本使用方法
### 生成 HEX 文件
在使用 STM32 ST-LINK Utility 之前，需要先通过编程工具（如 Keil 或 IAR）生成 HEX 文件。

- **Keil 生成 HEX 配置**：
  - 打开 Keil 工程，选择 `Project -> Options for Target -> Output`。
  - 勾选上“Create HEX File”。

- **IAR 生成 HEX 配置**：
  - 打开 IAR 工程，选择 `Project -> Options -> Output Converter`。
  - 勾选上“Generate additional output”，选择输出格式为“Intel extended”，设置输出名称。

### 连接 STM32 芯片
1. **硬件连接**：使用 ST-Link 连接硬件（STM32 芯片）。
2. **软件连接**：打开 STM32 ST-LINK Utility 软件，点击 `Target -> Connect` 或直接点击连接快捷按钮。
3. **读取 FLASH 信息**：连接成功后，可以读取 FLASH 信息、芯片型号、ID、版本等信息。

### 打开并下载程序
1. **打开 HEX 文件**：在连接好芯片并正确识别芯片之后，打开需要下载的程序（HEX）文件。可以通过菜单栏 `File -> Open File` 打开，也可以直接将 HEX 文件拖动到 FLASH 区域。
2. **下载程序**：打开 HEX 文件后，点击 `Target -> Program` 或直接点击下载快捷按钮。确认信息无误后点击“Start”开始下载程序。
3. **下载完成**：下载过程时间长短与程序大小有关，一般都很快。出现“Verification OK”说明下载成功。

## 总结
STM32 ST-LINK Utility 是一款功能强大的工具，适用于 STM32 微控制器的编程和调试。通过本文的介绍，您可以轻松掌握该工具的下载、安装和基本使用方法。希望本文对您的学习和开发有所帮助。

## 下载链接

[STM32ST-LINKUtility使用指南分享](https://pan.quark.cn/s/c3a10cd8c74a)