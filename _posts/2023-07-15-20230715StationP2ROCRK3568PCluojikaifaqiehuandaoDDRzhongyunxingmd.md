---
layout: post
title: "Station P2ROCRK3568PC 裸机开发切换到DDR中运行"
date:   2021-10-18
tags: [DDR,裸机,串口,初始化,RK3568]
comments: true
author: admin
---
# Station P2(ROC-RK3568-PC) 裸机开发：切换到DDR中运行

## 资源描述

本资源文件详细介绍了如何在 Station P2(ROC-RK3568-PC) 平台上进行裸机开发，并成功将代码切换到DDR中运行。由于无法在自定义的 tpl 中初始化DDR，因此我们改为编写 SPL（Secondary Program Loader）来实现这一目标。

### 主要内容

- **DDR初始化**：使用 `rk3568_ddr_1560MHz_v1.08.bin` 作为 tpl 来初始化内存。
- **SPL环境**：
  - 架构：AArch64
  - 异常级别：EL3
  - 内存：DDR
  - 入口地址：0x00000000
- **串口初始化**：代码运行后会先初始化 uart2 串口，以便进行调试和交互。
- **Mini Shell**：提供了一个简单的交互式 shell，支持以下指令：
  - `help`：显示帮助信息。
  - `exit`：退出 shell。
  - `hexDump`：以十六进制格式显示内存内容。
- **MASKROM模式**：输入 `q` 并回车，重复5次可以让设备回到 MASKROM 模式。
- **printf() 改进**：从这版开始，`printf()` 函数能够输出 `u64` 数据类型。

## 使用说明

1. **下载资源文件**：请从本仓库中下载相关资源文件。
2. **编译与烧录**：按照提供的文档和代码进行编译，并将生成的二进制文件烧录到设备中。
3. **运行与调试**：通过串口工具连接到 uart2，启动设备后即可进入 Mini Shell 进行交互和调试。

## 注意事项

- 确保设备处于 MASKROM 模式下进行烧录。
- 在调试过程中，注意观察串口输出，确保代码正确运行。

通过本资源文件，您可以深入了解如何在 Station P2(ROC-RK3568-PC) 平台上进行裸机开发，并成功将代码切换到DDR中运行。希望本资源对您的开发工作有所帮助！

## 下载链接

[StationP2ROC-RK3568-PC裸机开发切换到DDR中运行](https://pan.quark.cn/s/317a3ad33c6d)