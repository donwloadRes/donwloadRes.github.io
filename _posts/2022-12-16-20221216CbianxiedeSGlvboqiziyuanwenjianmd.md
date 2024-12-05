---
layout: post
title: "C编写的SG滤波器资源文件"
date:   2021-08-16
tags: [滤波器,C++,GSL,编写,编译]
comments: true
author: admin
---
# C++编写的S-G滤波器资源文件

## 简介

本仓库提供了一个使用C++编写的S-G滤波器资源文件。该滤波器基于Savitzky-Golay滤波方法，适用于对时间序列数据进行平滑处理。为了实现该滤波器，需要依赖GSL（GNU Scientific Library）库。

## 资源文件描述

- **标题**: C++编写S-G滤波
- **描述**: 使用C++编写的S-G滤波器，需要依赖GSL库。滤波方法的文献参考为Chen et al. 2004. A simple method for reconstructing a high-quality NDVI time-series data set based on the Savitzky–Golay filter. Remote Sensing of Environment。

## 使用说明

1. **依赖库**: 该滤波器依赖于GSL库，请确保在编译和运行代码之前已经安装并配置好GSL库。
2. **编译**: 使用C++编译器编译源代码，确保链接GSL库。
3. **运行**: 编译成功后，运行生成的可执行文件，输入需要处理的时间序列数据。

## 参考文献

Chen, J., Jönsson, P., Tamura, M., Gu, Z., Matsushita, B., & Eklundh, L. (2004). A simple method for reconstructing a high-quality NDVI time-series data set based on the Savitzky–Golay filter. Remote Sensing of Environment, 91(3-4), 332-344.

## 贡献

欢迎对本仓库进行贡献，包括但不限于代码优化、文档改进、错误修复等。请通过提交Pull Request的方式进行贡献。

## 许可证

本仓库的代码和资源文件遵循MIT许可证。详细信息请参阅LICENSE文件。

## 下载链接

[C编写的S-G滤波器资源文件](https://pan.quark.cn/s/5c27c342d6af)