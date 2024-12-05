---
layout: post
title: "VSCode 使用 g 编译 CC 文件指南"
date:   2023-12-20
tags: [++,VSCode,C++,编译,文件夹]
comments: true
author: admin
---
# VSCode 使用 g++ 编译 C/C++ 文件指南

本资源文件提供了在 Visual Studio Code (VSCode) 中使用 g++ 编译 C 文件或 C++ 文件的详细步骤和配置方法。通过本指南，您可以轻松地在 VSCode 中配置 g++ 编译环境，并进行 C/C++ 代码的编译和运行。

## 内容概述

1. **下载并配置 g++**
   - 下载 g++ 编译器（如 MinGW-W64 GCC-8.1）
   - 配置 g++ 的 bin 路径到系统环境变量
   - 验证 g++ 环境配置是否成功

2. **下载 VSCode 和相关插件**
   - 下载并安装 VSCode
   - 安装 Code Runner 插件和 C/C++ 插件

3. **在 VSCode 中设置 g++ 环境**
   - 创建工程文件夹并配置 `c_cpp_properties.json` 文件
   - 编写 C/C++ 代码并进行编译和运行

## 详细步骤

### 1. 下载并配置 g++

#### 1.1 下载 g++
- 从 Sourceforge 官网下载 MinGW-W64 GCC-8.1 编译器，选择 x86_64-win32-sjlj 版本。

#### 1.2 配置 g++
- 解压缩下载的压缩包，得到 mingw64 文件夹。
- 将 g++ 的 bin 路径（如 `I:\Profile\mingw64\bin`）添加到系统环境变量的 Path 中。

#### 1.3 验证 g++
- 打开命令提示符，输入 `g++ -v` 命令，查看 g++ 版本号以验证配置是否成功。

### 2. 下载 VSCode 和相关插件

#### 2.1 下载 VSCode
- 从 VSCode 官网下载并安装 VSCode。

#### 2.2 安装插件
- 在 VSCode 中安装 Code Runner 插件和 C/C++ 插件。

### 3. 在 VSCode 中设置 g++ 环境

#### 3.1 创建工程文件夹
- 新建一个文件夹（如 `hello`），并在其中创建 `vscode` 文件夹。
- 在 `vscode` 文件夹中创建 `c_cpp_properties.json` 文件，配置 g++ 路径和其他相关设置。

#### 3.2 编写代码并运行
- 在 `hello` 文件夹中创建 C/C++ 代码文件（如 `hello.cpp`）。
- 右击代码文件，选择“Run Code”进行编译和运行。

## 总结

通过以上步骤，您可以在 VSCode 中成功配置 g++ 编译环境，并进行 C/C++ 代码的编译和运行。希望本指南对您有所帮助！

## 下载链接

[VSCode使用g编译CC文件指南](https://pan.quark.cn/s/e8ad0f6064b7)