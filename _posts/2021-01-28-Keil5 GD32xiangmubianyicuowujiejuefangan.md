---
layout: post
title: "Keil5 GD32项目编译错误解决方案"
date:   2020-05-22
tags: [core,Keil5,编译,文件,项目]
comments: true
author: admin
---
# Keil5 GD32项目编译错误解决方案

## 资源文件介绍

本仓库提供了解决Keil5编译GD32项目时遇到的报错问题的资源文件。具体来说，该资源文件包括以下两个头文件：

- `core_cmInstr.h`
- `core_cmFunc.h`

## 问题描述

在使用Keil5编译GD32项目时，可能会遇到以下报错信息：

```
cannot open source input file “core_cmInstr.h”
cannot open source input file “core_cmFunc.h”
```

这些错误通常是由于项目中缺少必要的头文件导致的。

## 解决方案

为了解决上述问题，您可以将本仓库中的`core_cmInstr.h`和`core_cmFunc.h`文件添加到您的项目中。具体步骤如下：

1. 下载本仓库中的`core_cmInstr.h`和`core_cmFunc.h`文件。
2. 将这两个文件放置到您的项目目录中，确保它们位于正确的路径下。
3. 在Keil5中重新编译您的项目，错误应该会得到解决。

## 注意事项

- 请确保将这两个文件放置在正确的路径下，以便编译器能够正确找到它们。
- 如果您在其他项目中也遇到类似的问题，可以尝试使用本仓库中的资源文件进行解决。

希望本资源文件能够帮助您顺利解决Keil5编译GD32项目时遇到的报错问题。

## 下载链接

[Keil5GD32项目编译错误解决方案](https://pan.quark.cn/s/d4a23dd66fa8)