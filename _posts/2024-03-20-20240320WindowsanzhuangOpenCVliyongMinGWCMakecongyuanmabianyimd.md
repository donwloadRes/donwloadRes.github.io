---
layout: post
title: "Windows安装OpenCV利用MinGWCMake从源码编译"
date:   2022-09-18
tags: [OpenCV,编译,安装,CMake,contrib]
comments: true
author: admin
---
# Windows安装OpenCV——利用MinGW+CMake从源码编译

本资源文件提供了在Windows系统上使用MinGW和CMake从源码编译OpenCV的详细教程。通过本教程，您可以自定义OpenCV的安装选项，例如获取samples、交叉编译安装CUDA、安装contrib模块等。

## 教程内容概述

1. **准备工作**
   - 安装CMake：确保您已经安装了CMake，可以从CMake官网下载并安装。
   - 安装MinGW：建议通过Msys2安装MinGW，并将其路径添加到系统环境变量中。

2. **下载OpenCV源码**
   - 从OpenCV官方仓库下载所需版本的OpenCV源代码。
   - 如果需要安装contrib模块，请从OpenCV的contrib仓库下载相应版本的contrib包。

3. **使用CMake配置和编译**
   - 解压下载的OpenCV和contrib包到同一目录下。
   - 在OpenCV文件夹中新建一个build文件夹。
   - 打开CMake，选择源代码路径为OpenCV文件夹，生成二进制文件路径为build文件夹。
   - 点击开始编译（configure），选择makefile系统为MinGW。

4. **编译和安装**
   - 在build文件夹中打开cmd或终端，输入`mingw32-make`开始编译。
   - 编译完成后，输入`mingw32-make install`开始安装库。

5. **配置环境变量**
   - 添加OpenCV的库路径和路径到系统的环境变量中的PATH。
   - 确保系统能够找到编译后的OpenCV库。

## 常见问题

- **编译过程中文件下载失败**：如果在编译过程中某些文件下载失败，可以手动从GitHub或其他可靠来源下载这些文件，并进行替换。
- **编译选项自定义**：在CMake配置过程中，您可以根据需要自定义编译选项，例如选择编译Release版本或Debug版本，是否生成pkg-config文件等。

## 注意事项

- 如果安装OpenCV 4.5以上的版本，建议升级gcc的版本到最新版。
- 确保contrib模块的版本与OpenCV版本一致。

通过本教程，您可以顺利在Windows系统上从源码编译OpenCV，并根据需要自定义安装选项。

## 下载链接

[Windows安装OpenCV利用MinGWCMake从源码编译](https://pan.quark.cn/s/e45fa34f9216)