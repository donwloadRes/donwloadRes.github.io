---
layout: post
title: "ST-LINK Utility 4.6.0 下载安装及使用方法介绍"
date:   2021-08-31
tags: [ST,STM32,芯片,安装,hex]
comments: true
author: admin
---
# ST-LINK Utility 4.6.0 下载安装及使用方法介绍

## 简介
ST-LINK Utility 4.6.0 是一款针对STM32全系芯片进行编程（读、写、擦除、选项字）的工具。该软件主要用于量产（批量下载代码的工具），并且非常实用。当需要查看芯片FLASH数据时，可以快速定位并查找到想要的数据（前提是没有添加保护）。

## 主要功能
- **编程功能**：支持对STM32芯片进行读、写、擦除、选项字等操作。
- **量产工具**：适用于批量下载代码的场景。
- **数据查看**：可以快速查看芯片FLASH数据，便于调试和验证。

## 下载与安装
1. **下载地址**：
   - 官网下载地址：[ST官网](https://www.st.com/en/development-tools/stsw-link004.html)
   - 百度网盘地址：[百度网盘](https://pan.baidu.com/s/1mFlU5iBf6pznrGKOiC3iAw) 提取码：twsb

2. **安装步骤**：
   - 双击 `exe` 文件开始安装。
   - 进入安装向导，点击“Next”。
   - 同意许可协议，点击“Yes”。
   - 选择安装路径，点击“Next”。
   - 安装过程中会自动安装STLink驱动。
   - 安装完成后，点击“Finish”完成安装。

## 使用方法
1. **生成hex文件**：
   - **Keil配置**：Project -> Options for Target -> Output，勾选“Create HEX File”。
   - **IAR配置**：Project -> Options -> Output Converter，勾选“Generate additional output”，选择输出格式为“Intel extended”。

2. **连接芯片**：
   - 使用ST-Link连接硬件（STM32芯片）。
   - 打开STM32 ST-LINK Utility软件，连接芯片：Target -> Connect 或点击连接快捷按钮。

3. **打开程序（hex）**：
   - 连接好芯片并正确识别后，打开需要下载的程序（hex）文件。
   - 可以通过菜单栏（File -> Open File）打开，或直接将hex文件拖动到FLASH区域。

4. **下载程序（hex）**：
   - 打开hex文件后，点击“下载”（Target -> Program 或点击下载快捷按钮）。
   - 确认信息无误后，点击“Start”开始下载程序。

## 注意事项
- 安装STM32 ST-LINK Utility软件时，会自动安装STLink驱动，无需单独安装。
- 该软件支持Keil、IAR等工具的在线调试和下载。

## 版本信息
- 当前版本：4.6.0
- 查看版本：打开软件 -> Help -> About

## 总结
ST-LINK Utility 4.6.0 是一款功能强大的STM32编程工具，适用于量产和调试场景。通过简单的配置和操作，可以快速完成对STM32芯片的编程和数据查看。

## 下载链接

[ST-LINKUtility4.6.0下载安装及使用方法介绍](https://pan.quark.cn/s/4f6ed61c8c2d)