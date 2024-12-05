---
layout: post
title: "OpenCV 4.9.0 + 扩展模块 + WITH_QT（Qt6）模块编译教程（Windows）"
date:   2020-08-05
tags: [OpenCV,编译,Qt6,模块,Windows]
comments: true
author: admin
---
# OpenCV 4.9.0 + 扩展模块 + WITH_QT（Qt6）模块编译教程（Windows）

## 简介

本资源文件提供了在Windows系统上编译OpenCV 4.9.0及其扩展模块（contrib）的详细教程，并特别包含了WITH_QT（Qt6）模块的编译配置。通过本教程，您可以生成适用于Windows平台的OpenCV库，并支持Qt6的集成。

## 资源内容

- **OpenCV 4.9.0源码**：包含OpenCV核心库的源代码。
- **OpenCV扩展模块（contrib）源码**：包含额外的OpenCV功能模块。
- **WITH_QT（Qt6）模块编译配置**：详细指导如何在编译过程中集成Qt6。

## 编译环境

- **操作系统**：Windows 11（Windows 10也可使用）
- **编译器**：Mingw版本和MSVC19版本（支持Debug和Release模式）
- **Qt版本**：Qt6

## 前置要求

1. **翻墙能力**：由于编译过程中需要下载一些依赖库，建议具备翻墙能力以确保顺利下载。
2. **CMake**：用于配置和生成编译文件。
3. **编译工具**：Mingw或MSVC编译器。

## 编译步骤

### 1. 下载资源

- 下载OpenCV 4.9.0源码：[OpenCV GitHub](https://github.com/opencv/opencv)
- 下载OpenCV扩展模块（contrib）源码：[OpenCV Contrib GitHub](https://github.com/opencv/opencv_contrib)
- 下载Qt6：[Qt官方网站](https://www.qt.io/)

### 2. 配置编译环境

- 使用CMake配置OpenCV源码和扩展模块的路径。
- 配置WITH_QT选项，确保Qt6的路径正确设置。

### 3. 编译

- 使用CMake生成编译文件。
- 根据选择的编译器（Mingw或MSVC）进行编译。
- 编译完成后，生成OpenCV库文件。

### 4. 安装

- 将编译生成的库文件安装到指定目录。
- 配置开发环境，确保OpenCV库路径正确。

## 注意事项

- 编译过程中可能会遇到一些依赖库下载失败的问题，建议使用代理工具确保网络畅通。
- 编译过程中生成的库文件较多，建议根据实际需求选择性编译。

## 参考资料

- [OpenCV官方文档](https://docs.opencv.org/)
- [Qt官方文档](https://doc.qt.io/)

## 联系我们

如有任何问题或建议，请联系作者：charlie114514191@example.com

---

通过本教程，您将能够成功编译并使用OpenCV 4.9.0及其扩展模块，并集成Qt6进行开发。希望本资源对您的开发工作有所帮助！

## 下载链接

[OpenCV4.9.0扩展模块WITH_QTQt6模块编译教程Windows](https://pan.quark.cn/s/f7fff8bcbab5)