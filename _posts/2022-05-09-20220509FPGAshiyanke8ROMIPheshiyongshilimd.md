---
layout: post
title: "FPGA实验课8ROMIP核使用实例"
date:   2020-03-29
tags: [ROM,mif,IP,波形,文件]
comments: true
author: admin
---
# FPGA实验课8：ROM（IP核）使用实例

本资源文件提供了关于如何在FPGA中使用ROM（IP核）的详细实例。通过本教程，您将学习如何调用Quartus II自带的IP核生成ROM，并设置ROM存储的数值，以实现正弦波、三角波和锯齿波的输出。此外，本教程还将指导您如何使用在线逻辑分析工具Signal Tap观察波形。

## 实验要求

1. 调用Quartus II自带的IP核生成ROM。
2. 设置ROM存储的数值，实现正弦波、三角波和锯齿波的输出。
3. 使用在线逻辑分析工具Signal Tap观察波形。

## 实验步骤

### 1. ROM介绍

ROM（Read Only Memory）是一种只读存储器，其内容在任何情况下都不会改变。用户只能读取保存在ROM中的指令和资料，但不能变更或存入资料。ROM存储在非易失性芯片上，即使在关机后，记忆的内容仍可以被保存。ROM常用于存储特定功能的程序，如固件。

### 2. 生成波形数据文件

生成mif文件的方法有三种：
- 利用Quartus自带的mif编辑器
- 利用mif软件（如Mif_Maker2010）生成
- 利用高级语言生成

本教程使用第二种方法，通过Mif_Maker生成正弦波、三角波和锯齿波的mif文件。

### 3. Quartus配置ROM核并将mif文件加入工程

1. 找到ROM-1PORT并创建rom.v文件。
2. 配置ROM空间的位宽和字长。
3. 找到mif波形文件路径。
4. 将mif文件添加至工程。
5. 写地址控制器。
6. 调用ROM核。

### 4. 实验仿真

1. 新建testbeach文件。
2. 进行ModelSim仿真。

### 5. 在线逻辑分析

1. 新建STL文件。
2. 设置clk和数据分析长度。
3. 添加分析信号。
4. 保存文件并进行编译。
5. 添加设备。
6. 分析仿真。
7. 调制设置显示波形。

通过本教程，您将掌握如何在FPGA中使用ROM（IP核）生成和输出波形，并使用在线逻辑分析工具进行波形观察。

## 下载链接

[FPGA实验课8ROMIP核使用实例](https://pan.quark.cn/s/b6f0fe5f0997)