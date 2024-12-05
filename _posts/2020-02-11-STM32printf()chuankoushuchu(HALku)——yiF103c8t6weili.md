---
layout: post
title: "STM32printf()串口输出(HAL库)——以F103c8t6为例"
date:   2021-12-10
tags: [串口,printf,CubeMX,函数,HAL]
comments: true
author: admin
---
# STM32printf()串口输出(HAL库)——以F103c8t6为例

## 简介
在使用传感器测量数据时，通常需要对测量的数据进行显示。常见的显示方法有两种：一种是通过屏幕显示，另一种是通过串口将数据发送给上位机，在电脑上直接查看需要显示的数据内容。本文介绍了一种使用`printf()`函数通过串口输出数据的方法，并以STM32F103C8T6为例，详细说明了如何使用CubeMX进行配置，使`printf()`函数能够正常工作。

## 资源内容
本仓库提供的资源文件包含以下内容：
1. **CubeMX工程文件**：用于配置STM32F103C8T6的串口和相关外设。
2. **完整的工程文件**：包含使用`printf()`函数进行串口输出的代码示例。
3. **README.md**：本文件，提供了资源的使用说明和注意事项。

## 使用说明
1. **CubeMX配置**：
   - 使用CubeMX打开提供的工程文件，配置STM32F103C8T6的串口和相关外设。
   - 在`Project Manager`选项卡中，确保生成的代码包含必要的HAL库支持。

2. **代码修改**：
   - 在主程序中添加以下代码，以支持`printf()`函数的使用：
     ```c
     #include <stdio.h>

     int _write(int file, char *ptr, int len) {
         HAL_UART_Transmit(&huart1, (uint8_t *)ptr, len, HAL_MAX_DELAY);
         return len;
     }
     ```
   - 在`main.c`文件中包含头文件`<stdio.h>`。

3. **启用MicroLIB**：
   - 在CubeMX中，进入`Project Manager` -> `Code Generator`，勾选`Use MicroLIB`选项，以启用MicroLIB库，确保`printf()`函数能够正常工作。

4. **编译与下载**：
   - 使用Keil或其他支持的IDE打开生成的工程文件，编译并下载到STM32F103C8T6开发板上。

5. **串口调试**：
   - 使用串口调试工具（如Putty、Tera Term等）连接到开发板的串口，设置波特率等参数，即可通过`printf()`函数输出数据到上位机。

## 注意事项
- 在使用`printf()`函数时，确保在CubeMX中勾选了`Use MicroLIB`选项，否则`printf()`函数可能无法正常工作。
- 本资源文件中的代码和配置仅供参考，用户可以根据自己的需求进行修改和扩展。
- 如果遇到任何问题，请参考STM32的官方文档或相关论坛进行排查。

## 总结
通过本资源文件，您可以快速上手使用`printf()`函数在STM32F103C8T6上进行串口输出。希望本资源能够帮助您在传感器数据采集和显示方面取得进展。

## 下载链接

[STM32printf串口输出HAL库以F103c8t6为例](https://pan.quark.cn/s/c82994f007f1)