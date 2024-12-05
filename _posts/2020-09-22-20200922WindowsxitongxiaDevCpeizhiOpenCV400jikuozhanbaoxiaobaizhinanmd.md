---
layout: post
title: "Windows系统下DevC配置OpenCV 400及扩展包小白指南"
date:   2020-09-28
tags: [OpenCV,C++,Dev,4.0,Windows]
comments: true
author: admin
---
# Windows系统下Dev-C++配置OpenCV 4.0.0及扩展包——小白指南

## 简介

本资源文件旨在帮助初学者在Windows系统下使用Dev-C++配置OpenCV 4.0.0及其扩展包。无论你是刚刚接触C++编程，还是希望在Dev-C++中集成OpenCV进行图像处理，本指南都将为你提供详细的步骤和必要的软件下载链接。

## 准备工作

在开始配置之前，请确保你已经准备好以下软件和工具：

1. **Dev-C++**：一个轻量级的C++集成开发环境（IDE）。
2. **CMake**：用于构建OpenCV的跨平台工具。
3. **OpenCV 4.0.0**：开源计算机视觉库的源码。
4. **OpenCV Contrib**：OpenCV的扩展模块，包含了一些额外的功能。

## 配置步骤

### 步骤一：Dev-C++安装

1. 下载并安装Dev-C++。
2. 确保系统环境变量PATH中添加了Dev-C++的MinGW64\bin路径。

### 步骤二：CMake安装

1. 下载并安装CMake。
2. 在系统环境变量PATH中添加CMake的bin路径。

### 步骤三：解压OpenCV和OpenCV Contrib

1. 下载OpenCV 4.0.0源码和OpenCV Contrib扩展包。
2. 将它们解压到同一个文件夹中，并在该文件夹下创建一个名为`build`的文件夹。

### 步骤四：使用CMake配置OpenCV

1. 打开CMake GUI，设置源码路径和构建路径。
2. 点击`Configure`，选择`MinGW Makefiles`作为生成器。
3. 在配置过程中，可能会遇到需要下载外部库的问题，根据提示手动下载并放置到指定位置。
4. 勾选`WITH_OPENGL`，不勾选`WITH_IPP`和`WITH_MSMF`，启用预编译头文件，并设置`OPENCV_EXTRA_MODULES_PATH`为OpenCV Contrib的modules路径。
5. 继续点击`Configure`直至所有选项变白，然后点击`Generate`生成Makefile。

### 步骤五：使用MinGW编译OpenCV

1. 打开命令提示符，进入OpenCV的build文件夹。
2. 输入`mingw32-make`命令进行编译，完成后输入`mingw32-make install`进行安装。

### 步骤六：Dev-C++配置OpenCV

1. 打开Dev-C++，进入工具栏的编译器选项。
2. 在编译器选项中，勾选`-std=c++11`，并在链接器选项中添加OpenCV的库文件路径和库名称。

## 结语

通过以上步骤，你应该能够在Windows系统下成功配置Dev-C++与OpenCV 4.0.0及其扩展包。如果在配置过程中遇到任何问题，可以参考CSDN博客中的详细步骤进行排查。祝你配置顺利，编程愉快！

## 下载链接

[Windows系统下Dev-C配置OpenCV4.0.0及扩展包小白指南分享](https://pan.quark.cn/s/351e7e11d3d1)