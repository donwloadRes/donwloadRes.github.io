---
layout: post
title: "基于MATLAB的数字带通传输系统仿真实验（BPSK调制与解调）"
date:   2024-06-30
tags: [载波,10,码元,MATLAB,BPSK]
comments: true
author: admin
---
# 基于MATLAB的数字带通传输系统仿真实验（BPSK调制与解调）

## 项目描述

本资源文件提供了一个基于MATLAB的数字带通传输系统仿真实验，主要涉及BPSK（二进制相移键控）调制与解调的实现。实验内容包括以下几个部分：

1. **随机二进制码元序列生成**：
   - 生成一个长度为100的随机二进制码元序列。

2. **BPSK调制波形及其功率谱**：
   - 假设载波频率为 `fc`（单位：Hz），码元传输速率为 `RB`（单位：Baud），码元持续时间为 `Ts`（单位：s）。
   - 当 `fc = 10RB` 时，绘制采样率为 `100Sample/Ts` 的BPSK调制波形（前10个码元）及其功率谱。

3. **相干解调（收发载波频率相同，初相位均为0）**：
   - 假设收发载波频率相同均为 `fc = 10RB`，初相位均为0。
   - 绘制 `x(t)` 的波形，并假设低通滤波器的冲激响应分别为连续10个1（其余为0）和连续12个1（其余为0），分别绘制两种滤波器下的 `y(t)` 及判决输出（前10个码元）。

4. **相干解调（收发载波频率相同，接收端初相位为π）**：
   - 假设收发载波频率相同均为 `fc = 10RB`，发端初相为0，接收端初相位为π。
   - 绘制 `x(t)` 的波形，并假设低通滤波器的冲激响应为连续10个1（其余为0），绘制此滤波器下的 `y(t)` 及判决输出（前10个码元）。

5. **接收载波频率偏移**：
   - 假设发送载波频率不变仍为 `fc = 10RB`，接收载波频率为 `10.05RB`，初相位均为0。
   - 绘制 `x(t)` 的波形，并假设低通滤波器的冲激响应为连续10个1（其余为0），绘制此滤波器下的 `y(t)` 及判决输出（前10个码元）。

6. **DPSK及延时**：
   - 采用DPSK（差分相移键控）及延时进行进一步的仿真实验。

## 使用说明

1. **环境要求**：
   - MATLAB R2016b及以上版本。

2. **文件结构**：
   - `main.m`：主程序文件，包含所有实验步骤的代码。
   - `utils.m`：辅助函数文件，包含一些常用的函数。

3. **运行步骤**：
   - 打开MATLAB，将项目文件夹添加到路径中。
   - 运行 `main.m` 文件，程序将依次执行所有实验步骤，并生成相应的图形结果。

## 注意事项

- 本实验假设了一些理想条件，如无噪声、无多径效应等。实际应用中可能需要考虑更多的因素。
- 实验结果仅供参考，具体应用时请根据实际情况进行调整。

## 贡献

欢迎对本项目进行改进和扩展，如果您有任何建议或发现问题，请提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅 `LICENSE` 文件。

## 下载链接

[基于MATLAB的数字带通传输系统仿真实验BPSK调制与解调](https://pan.quark.cn/s/a59d61a72231)