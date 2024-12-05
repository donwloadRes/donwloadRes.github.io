---
layout: post
title: "Linux安装CMake、Eigen与osqp库指南"
date:   2022-11-18
tags: [CMake,安装,Linux,osqp,Eigen]
comments: true
author: admin
---
# Linux安装CMake、Eigen与osqp库指南

## 概述

本资源提供了详尽的指导，旨在帮助用户在Linux环境下顺利安装CMake、Eigen和osqp库，并介绍了如何使用这些库。这些库对于进行计算机视觉、机器学习、优化等领域的软件开发至关重要。以下是逐步安装教程的摘要，源自[CSDN博客](https://blog.csdn.net/weixin_44516295/article/details/131138357)，该教程特别适用于Ubuntu 18.04用户，但大多数步骤在其他Linux发行版上也可行。

## 环境需求

- **操作系统**: Ubuntu 18.04 或更高版本
- **CMake版本**: 至少3.14以上

## 安装步骤

### 1. CMake安装

1. 更新系统包。
2. 下载CMake源码包，如版本3.22.1。
3. 解压，进入目录，赋予执行权限，配置并编译。
4. 完成安装并设置系统默认CMake版本。

### 2. Eigen安装

1. 下载Eigen 3.4.0的源码。
2. 解压，进入`eigen-3.4.0`，创建并进入`build`目录。
3. 使用CMake配置，然后执行make与sudo make install。
4. 将Eigen头文件拷贝至系统目录。

### 3. osqp库安装

1. 下载osqp源码，同样解压并进入`build`流程。
2. 使用CMake配置，并指定安装前缀，随后进行编译与安装。

### 4. osqp-eigen库安装

1. 获取osqp-eigen的源代码。
2. 类似地，在其源代码的`build`目录下执行相同的CMake和安装命令。

### 5. 测试安装

- 下载测试代码，调整CMakeLists.txt中的库路径。
- 编译并运行测试程序，确认所有库都正确安装并可被程序链接。

## 注意事项

- 每个库的安装过程中，确保遵循正确的CMake命令与参数，特别是版本指定项。
- 自动化脚本或图形界面工具可能简化安装过程，但对于自定义安装路径或特定版本需求，手动安装更为可靠。
- 完成安装后，可能需要更新环境变量，确保系统能够找到新的库文件。

通过遵循上述步骤，您应该能够在Linux系统上成功安装并开始利用这些强大的开发库。记得在实际应用中测试库的兼容性和功能性，以保障项目的顺利进展。

## 下载链接

[Linux安装CMakeEigen与osqp库指南](https://pan.quark.cn/s/eacfa7f50220)