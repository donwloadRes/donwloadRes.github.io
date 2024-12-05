---
layout: post
title: "STM32F103C8T6 HAL库例程：点灯与串口通信"
date:   2021-12-12
tags: [串口,STM32F103C8T6,LED,字符,DMA]
comments: true
author: admin
---
# STM32F103C8T6 HAL库例程：点灯与串口通信

## 简介

本仓库提供了基于STM32F103C8T6微控制器的HAL库例程，主要包含以下三个代码程序：

1. **点亮LED灯**：演示如何使用HAL库控制STM32F103C8T6的GPIO引脚，实现LED灯的点亮与熄灭。

2. **串口通信（不定长发送字符）**：通过串口通信实现不定长字符的发送，并以特定字符作为发送结束的标志。

3. **串口通信（DMA方式+空闲中断）**：使用DMA方式和空闲中断实现不定长字符的串口通信，提高数据传输效率。

## 目录结构

```
├── LED_Blink/
│   ├── Core/
│   ├── Drivers/
│   ├── Makefile
│   └── README.md
├── UART_Variable_Length/
│   ├── Core/
│   ├── Drivers/
│   ├── Makefile
│   └── README.md
├── UART_DMA_Idle_Interrupt/
│   ├── Core/
│   ├── Drivers/
│   ├── Makefile
│   └── README.md
└── README.md
```

## 使用说明

### 1. 点亮LED灯

- **目录**: `LED_Blink/`
- **功能**: 控制STM32F103C8T6的GPIO引脚，实现LED灯的闪烁。
- **使用方法**: 
  1. 打开`LED_Blink/`目录下的工程文件。
  2. 编译并下载到STM32F103C8T6开发板。
  3. 观察LED灯的闪烁效果。

### 2. 串口通信（不定长发送字符）

- **目录**: `UART_Variable_Length/`
- **功能**: 通过串口发送不定长字符，并以特定字符作为发送结束标志。
- **使用方法**:
  1. 打开`UART_Variable_Length/`目录下的工程文件。
  2. 编译并下载到STM32F103C8T6开发板。
  3. 使用串口调试工具接收数据，观察发送的字符。

### 3. 串口通信（DMA方式+空闲中断）

- **目录**: `UART_DMA_Idle_Interrupt/`
- **功能**: 使用DMA方式和空闲中断实现不定长字符的串口通信，提高数据传输效率。
- **使用方法**:
  1. 打开`UART_DMA_Idle_Interrupt/`目录下的工程文件。
  2. 编译并下载到STM32F103C8T6开发板。
  3. 使用串口调试工具接收数据，观察发送的字符。

## 依赖

- STM32CubeMX
- STM32 HAL库
- Keil MDK 或 STM32CubeIDE

## 贡献

欢迎提交Issue和Pull Request，共同完善本仓库的代码和文档。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[STM32F103C8T6HAL库例程点灯与串口通信](https://pan.quark.cn/s/337bcaa44df5)