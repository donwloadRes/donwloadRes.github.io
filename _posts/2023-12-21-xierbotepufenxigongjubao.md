---
layout: post
title: "希尔伯特谱分析工具包"
date:   2021-12-27
tags: [工具包,文件,希尔伯特,Spectrum,Instantaneous]
comments: true
author: admin
---
# 希尔伯特谱分析工具包

## 简介

本仓库提供了一个封装好的希尔伯特谱分析工具包，包含以下功能：

- 希尔伯特谱（Hilbert Spectrum）
- 边际谱（Marginal Spectrum）
- 包络谱（Envelope Spectrum）
- 瞬时频率（Instantaneous Frequency）
- 瞬时幅值（Instantaneous Amplitude）
- 瞬时相位（Instantaneous Phase）

所有功能均封装在`.p`文件中，用户可以直接调用并运行。工具包中调用了`hhtSpec`、`marginalSpec`、`envSpec`、`InsFPA`、`pEMDandFFT`等函数，方便用户进行信号分析。

## 使用说明

1. **下载文件**：请下载本仓库中的所有`.p`文件。
2. **导入文件**：将下载的`.p`文件导入到您的MATLAB工作环境中。
3. **调用函数**：根据您的需求，直接调用相应的函数进行信号分析。

## 注意事项

- 本工具包适用于MATLAB环境，请确保您的MATLAB版本支持`.p`文件的调用。
- 在使用过程中，请确保所有依赖函数（如`hhtSpec`、`marginalSpec`等）均已正确导入。

## 贡献

如果您在使用过程中发现任何问题或有改进建议，欢迎提交Issue或Pull Request。

## 许可证

本工具包遵循MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[希尔伯特谱分析工具包](https://pan.quark.cn/s/86a8604ce2d9)