---
layout: post
title: "最新Win11编译CloudCompare2.12.2逐步教程【含PCL和PDAL的安装】"
date:   2021-02-24
tags: [教程,编译,安装,CloudCompare,PCL]
comments: true
author: admin
---
# 最新Win11编译CloudCompare2.12.2逐步教程【含PCL和PDAL的安装】

本仓库提供了一个详细的教程，帮助用户在Windows 11系统上编译CloudCompare 2.12.2版本，并包含PCL（Point Cloud Library）和PDAL（Point Data Abstraction Library）的安装步骤。

## 内容概述

本教程分为以下几个主要部分：

1. **编译准备工作**：
   - 下载并安装Visual Studio 2022
   - 下载并安装CMake
   - 下载并安装Qt 5.15.2
   - 下载并安装PCL 1.12.0
   - 下载并安装PDAL

2. **CloudCompare源码下载**：
   - 使用Git Bash克隆CloudCompare 2.12.2版本的源码

3. **编译过程**：
   - 使用CMake配置和生成项目文件
   - 使用Visual Studio 2022进行编译
   - 配置环境变量
   - 生成可执行文件并运行

4. **点云重建相关依赖安装**：
   - 安装CGAL库以支持得劳内三角剖分功能

## 使用说明

1. **下载资源文件**：
   - 下载本仓库提供的资源文件，包含所有必要的安装包和源码。

2. **按照教程步骤操作**：
   - 按照教程中的步骤，逐步完成CloudCompare 2.12.2的编译和安装。

3. **检查环境变量**：
   - 确保所有环境变量配置正确，并重启电脑使环境变量生效。

4. **运行CloudCompare**：
   - 编译完成后，运行生成的CloudCompare可执行文件，检查是否支持pcd和las格式的点云读取。

## 注意事项

- 本教程适用于Windows 11系统，其他系统可能需要调整部分步骤。
- 编译过程中如遇到问题，请参考错误列表定位并解决问题。
- 确保所有依赖库版本与教程中一致，以避免兼容性问题。

## 更新记录

- 2023-10-08：首次发布
- 2023-10-24：更新部分内容，修复已知问题

## 参考资料

- CloudCompare官方编译指导
- Visual Studio 2022安装与使用教程
- Windows下CMake安装教程
- VisualStudio如何配置PCL点云库
- 最具体和最简单的PDAL库配置及在VS2019上测试

## 联系我们

如有任何问题或建议，请通过GitHub Issues联系我们。

## 下载链接

[最新Win11编译CloudCompare2.12.2逐步教程含PCL和PDAL的安装](https://pan.quark.cn/s/5696ab742f56)