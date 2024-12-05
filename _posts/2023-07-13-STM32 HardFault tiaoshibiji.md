---
layout: post
title: "STM32 HardFault 调试笔记"
date:   2024-01-08
tags: [STM32,HardFault,调试,笔记,Keil]
comments: true
author: admin
---
# STM32 HardFault 调试笔记

## 简介
本资源文件提供了关于STM32 HardFault调试的详细笔记。HardFault是STM32微控制器在执行过程中遇到的一种严重异常，通常表示处理器检测到无法恢复的错误，导致程序无法继续正常运行。理解并诊断STM32 HardFault对于开发者来说至关重要，因为这有助于识别和修复程序中的错误。

## 内容概述
本笔记涵盖了以下几个关键部分：

1. **必备知识点**：
   - 在Keil对STM32的程序进行仿真时，程序有时会跑飞，停止仿真程序会停在HardFault_Handler函数里的死循环while(1)中。
   - 说明STM32出现了硬件错误，遇到这种问题时，应该怎么调试并定位触发硬件错误的位置。

2. **基础知识讲解**：
   - Fault类异常：包括总线faults、存储器管理faults、用法faults和硬fault。
   - 总线Faults：当AHB接口上正在传送数据时，如果回复了一个错误信号，则会产生总线faults。
   - 存储器管理Faults：多与MPU有关，其诱因常常是某次访问触犯了MPU设置的保护策略。
   - 用法Faults：发生的场合可以是执行了未定义的指令、执行了协处理器指令等。
   - 硬Fault：是上文讨论的总线fault、存储器管理fault以及用法fault上访的结果。

3. **实操**：
   - 在硬件中断函数HardFault_Handler里的while(1)处打调试断点，程序执行到断点处时点击“STOP”停止仿真。
   - 查看具体错误原因，使用Keil仿真时的错误报告寄存器Peripherals->Core Peripherals->Fault Reports。
   - 在Keil菜单栏点击“View”——“Registers Window”，在寄存器查看窗口查找R14(LR)的值，确定当前使用堆栈为MSP或PSP。
   - 在Keil菜单栏点击“View”——“Memory Windows”——“Memory1”，在“Address”地址栏中输入MSP的值，然后在对应的行里找到地址。
   - 在Keil菜单栏点击“View”——“Disassembly Window”，在“Disassembly”窗口中右击，在下拉菜单中选择“Show Disassembly at Address”，在弹出框“Show Code at Address”的地址框中输入地址进行搜索，然后就会找到相对应的代码。

## 错误原因
常见的错误原因包括：
- 数组越界操作
- 内存溢出，访问越界
- 堆栈溢出，程序跑飞
- 中断处理错误

## 使用方法
1. 下载本资源文件。
2. 阅读笔记中的详细步骤和解释。
3. 根据笔记中的指导，进行实际的调试操作。

## 注意事项
- 在进行调试时，务必确保使用正确的调试工具和环境。
- 仔细检查代码，确保没有明显的错误。
- 如果遇到问题，可以参考笔记中的错误原因和解决方法。

希望本笔记能够帮助您更好地理解和解决STM32 HardFault问题。

## 下载链接

[STM32HardFault调试笔记](https://pan.quark.cn/s/409910d9bb49)