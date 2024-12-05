---
layout: post
title: "Xilinx Vivado-Vitis 2020.1 MicroBlaze工程教程"
date:   2020-09-22
tags: [MicroBlaze,Vivado,教程,固化,SPI]
comments: true
author: admin
---
# Xilinx Vivado/Vitis 2020.1 MicroBlaze工程教程

本教程详细介绍了如何使用Xilinx Vivado 2020.1和Vitis 2020.1创建一个最简单的MicroBlaze工程，运行Hello World C语言程序，并且不使用外部DDR3内存，最终将程序固化到SPI Flash中。

## 教程内容概述

1. **创建MicroBlaze工程**：
   - 使用Xilinx Vivado 2020.1创建一个空白的工程。
   - 添加MicroBlaze IP核并配置其运行内存为128KB。
   - 配置时钟和复位信号。

2. **添加外设**：
   - 添加AXI Uartlite串口IP核，用于程序中的printf打印和scanf输入。
   - 配置串口的波特率为115200。

3. **生成Block Design**：
   - 自动生成Block Design并创建Verilog顶层模块。
   - 综合并绑定FPGA管脚。

4. **固化程序到SPI Flash**：
   - 在Vivado中生成bit文件并导出xsa文件。
   - 在Vitis中创建Platform Project和Application Project。
   - 将程序固化到SPI Flash中，确保断电后程序仍能启动运行。

## 注意事项

- 本教程不使用外部DDR3内存，所有程序运行在FPGA片内的BRAM中。
- 固化程序到SPI Flash时，需确保在Vivado工程的xdc文件中添加SPI 4位模式的配置，以避免开机启动缓慢。

## 适用开发板

本教程以米联客XC7A35T FGG484-2开发板为例，但步骤适用于其他支持MicroBlaze的开发板。

## 参考资料

本教程参考了CSDN博客上的详细文章，内容涵盖了从工程创建到程序固化的完整操作步骤。

---

通过本教程，您将能够掌握使用Xilinx Vivado和Vitis创建并固化MicroBlaze工程的基本技能。

## 下载链接

[XilinxVivadoVitis2020.1MicroBlaze工程教程](https://pan.quark.cn/s/5e35d2b7729d)