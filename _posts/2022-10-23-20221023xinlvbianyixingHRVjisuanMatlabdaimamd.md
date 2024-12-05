---
layout: post
title: "心率变异性（HRV）计算Matlab代码"
date:   2022-05-24
tags: [HRV,心率,代码,计算,Matlab]
comments: true
author: admin
---
# 心率变异性（HRV）计算Matlab代码

## 资源描述

本仓库提供了一个用于心率变异性（HRV）计算的Matlab代码。该代码主要用于处理单引线原始Zio贴片ECG信号，并通过改进的Pan-Tompkins、主成分分析和抛物线拟合算法进行R峰检测，进而计算心率和HRV参数。

## 目录结构

- **R_peak_detector**: 用于R峰检测的代码。运行`Main.m`文件以计算R峰，并选择一个3分钟的正弦信号。
- **HRV_full**: 在运行R峰检测代码之后，运行此文件夹中的`Main.m`文件以计算心率和HRV参数。

## 代码功能

### R峰检测

- **算法**: 使用改进的Pan-Tompkins、主成分分析和抛物线拟合算法进行R峰检测。
- **RR间隔判断**: 如果RR间隔的持续时间在上一个RR间隔的持续时间的15%以内，则将RR间隔视为窦性。

### HRV分析

- **参数计算**: 代码将计算心率和HRV参数，包括RMSSD、LF、HF、LF/HF、SD1、SD2、SD1/SD2、样本熵、仁义熵等。

## 测试文件

- **数据集**: 提供了来自单线索ZioPatch的9个小时的原始数据，文件名为`130812_Z320892913_1563`。
- **脱识别数据集**: 提供了完全脱识别的数据集，文件名为`PACE脱识别ECGpatchHRV数据集28pts.xls`。

## 作者

- **Muammar Kabir, 博士**
- **Nichole Rogovoy, BSE**
- **Erick**

## 版本

- **V.1**

## 使用说明

1. 首先运行`R_peak_detector`文件夹中的`Main.m`文件，进行R峰检测。
2. 然后运行`HRV_full`文件夹中的`Main.m`文件，计算心率和HRV参数。

## 注意事项

- 确保Matlab环境已正确配置。
- 数据集文件路径需正确设置。

通过本代码，您可以有效地计算心率变异性参数，并应用于相关研究或项目中。

## 下载链接

[心率变异性HRV计算Matlab代码](https://pan.quark.cn/s/58608985cd57)