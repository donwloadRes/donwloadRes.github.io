---
layout: post
title: "解决 Microsoft Visual C 140 或更高版本需求的方法"
date:   2023-03-05
tags: [C++,编译,Microsoft,安装,版本]
comments: true
author: admin
---
# 解决 Microsoft Visual C++ 14.0 或更高版本需求的方法

本文档提供了解决在安装某些Python包时遇到的“Microsoft Visual C++ 14.0 or greater is required”错误的方法。该错误通常是由于缺少必要的C++编译环境导致的。

## 问题描述

在使用pip安装某些Python包时，可能会遇到以下错误提示：
```
error: Microsoft Visual C++ 14.0 or greater is required. Get it with “Microsoft C++ Build Tools”
```
这是因为这些包需要使用C++编译后才能正常安装，但当前环境中缺少完整的C++编译环境。

## 解决方案

### 1. 下载并安装 Microsoft C++ Build Tools

1. 打开以下网址下载Microsoft C++ Build Tools：
   ```
   https://visualstudio.microsoft.com/visual-cpp-build-tools/
   ```
2. 点击下载“生成工具”并打开。
3. 在“工作负荷”中，选择“C++ build tools”。
4. 在“单个组件”中，选择所需的C++工具并开始下载。

### 2. 重启计算机

下载完成后，重启计算机以确保所有更改生效。

### 3. 使用WHL版本（可选）

如果无法正常完成编译，可以尝试使用对应包的WHL版本进行安装。WHL版本是预编译版本，可以避免安装C++编译环境。

## 注意事项

- 该方法适用于大多数需要C++编译环境的Python包。
- 如果某些包没有WHL版本，建议安装完整的C++编译环境以确保兼容性。

通过上述步骤，你应该能够解决由缺少Microsoft Visual C++ 14.0或更高版本引起的安装问题，并成功安装所需的Python包。

## 下载链接

[解决MicrosoftVisualC14.0或更高版本需求的方法](https://pan.quark.cn/s/b4e1e42fdcbf)