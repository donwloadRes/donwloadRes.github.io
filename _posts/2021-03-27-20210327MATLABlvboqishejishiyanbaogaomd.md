---
layout: post
title: "MATLAB滤波器设计实验报告"
date:   2022-02-09
tags: [滤波器,函数,MATLAB,实验报告,FIR]
comments: true
author: admin
---
# MATLAB滤波器设计实验报告

## 资源文件介绍

本仓库提供了一个名为 `MAtlab窗函数法和双线性变换法设计FIR滤波器和IIR滤波器-DSP.doc` 的资源文件。该文件是我以前在数字信号处理（DSP）课程中的实验报告，主要内容包括使用MATLAB进行FIR和IIR滤波器的设计，并通过窗函数法和双线性变换法实现。

## 文件内容概述

### 实验目标

1. 采集单声道音频信号（.wav格式）并使用 `wavread` 函数进行采样读取。
2. 对音频信号进行频谱分析。
3. 分别使用窗函数法和双线性变换法设计低通、高通、带通三种FIR滤波器和IIR滤波器。
4. 通过MATLAB脚本使信号通过滤波器，并对输出信号进行时域和频域分析。

### 实验步骤

1. **设计FIR滤波器**：
   - 先将期望数字滤波器的指标通过预畸变转化为模拟滤波器的指标。
   - 使用MATLAB函数得到模拟滤波器的传输函数。
   - 通过双线性变换法得到数字滤波器的传输函数。

2. **设计IIR滤波器**：
   - 通过数字滤波器指标得到窗函数的阶数和系数。
   - 得到数字滤波器的传输函数。

## 注意事项

- 由于单声道音频信号无法上传，建议自行采集并进行实验。
- 本实验报告仅供参考，程序可能存在不当之处，请谨慎使用。

## 适用人群

本资源适用于正在学习数字信号处理（DSP）课程的学生，尤其是需要进行滤波器设计实验的同学们。希望这份实验报告能够为你的学习提供一些帮助。

## 贡献与反馈

如果你在使用过程中发现任何问题或有改进建议，欢迎通过GitHub的Issues功能提出。感谢你的支持与反馈！

## 下载链接

[MATLAB滤波器设计实验报告分享](https://pan.quark.cn/s/55af7b164c67)