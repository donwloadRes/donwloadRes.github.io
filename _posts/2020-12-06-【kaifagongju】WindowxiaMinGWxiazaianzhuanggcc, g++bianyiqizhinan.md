---
layout: post
title: "【开发工具】Window下MinGW下载安装gcc, g++编译器指南"
date:   2020-05-13
tags: [gcc,MinGW,---,++,编译]
comments: true
author: admin
---
# 【开发工具】Window下MinGW下载安装gcc, g++编译器指南

---

## 简介

本文档提供了详细的步骤，帮助您在Windows操作系统上下载和安装MinGW，以及配置gcc和g++编译器。MinGW是Minimalist GNU for Windows的缩写，它让您能够在没有Linux仿真层（如Cygwin）的情况下，直接在Windows平台上编译GCC支持的各种语言程序，尤其是专注于C和C++。

---

## 必备知识

- 选择与您的Java JDK位数相匹配的MinGW版本（32位或64位），确保编译出的库文件与JVM兼容。
- Linux编译的程序不能在Windows上运行，反之亦然；同样，不同位数的Windows系统需要相应位数的程序。

---

## 下载MinGW

- **64位**: 可访问SourceForge项目的 MingW-w64 或者寻找可靠的第三方镜像。
- **32位**: 使用原始MinGW项目页面获取。

---

## 安装步骤

1. **下载安装包**：根据需要选择对应位数的MinGW-get setup程序。
2. **运行安装**：指定安装目录，推荐自定义以便管理。
3. **通过MinGW Installation Manager**：
   - 勾选`mingw32-gcc-g++-bin`以安装gcc和g++。
   - 应用更改，耐心等待下载与安装完成。
4. **环境变量配置**：
   - 添加MinGW的`bin`目录（如`E:\dev_tools\MinGW\bin`）到系统PATH中。

---

## 验证安装

- 打开命令提示符，输入`gcc -v`和`g++ -v`，检查版本信息以确认安装成功。

---

## 使用MinGW

- 示例：编译一个简单的C程序。
- 步骤：编写代码 -> 使用`gcc 文件名.c -o 输出文件名`编译 -> 运行生成的.exe文件。

---

## 生成动态链接库

- 对于需要编译DLL的开发者，本文档还简述了如何使用gcc命令行生成动态链接库，涉及到特定的编译选项和库路径配置。

---

## 编译器区别

- **gcc vs g++**：尽管gcc能够编译C和C++代码，但对于C++项目推荐使用g++，因为它能自动链接C++库。
- **cc与CC**：cc通常是gcc的别名，用于向后兼容Unix; CC在makefile中常用来指定编译器，默认可设为gcc或g++。

---

## 注意事项

- 解决安装过程中可能出现的依赖问题，如缺少某些包，可能需要手动下载或从相似环境迁移相关dll文件。
- 确保正确配置环境变量，避免因路径错误而导致的编译命令不可用。

---

通过跟随上述指南，您可以顺利在Windows环境下设置好C和C++的开发环境，开始您的编码之旅。如果遇到特定问题，查阅官方网站和社区文档往往会提供解决方案。祝您开发愉快！

## 下载链接

[开发工具Window下MinGW下载安装gcc分享](https://pan.quark.cn/s/a0bf9697e091)