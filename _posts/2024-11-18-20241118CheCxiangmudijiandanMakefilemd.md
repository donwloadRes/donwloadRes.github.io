---
layout: post
title: "C 和 C++ 项目的简单 Makefile"
date:   2023-05-29
tags: [Makefile,DIR,文件目录,编译器,源文件]
comments: true
author: admin
---
# C 和 C++ 项目的简单 Makefile

这个仓库提供了一个简单的 Makefile，适用于 C 和 C++ 项目。该 Makefile 可以在 Linux 和 Windows 上使用 Mingw 进行编译。它为源文件和头文件使用单独的目录，并递归地查找其中的每个文件，因此您不必自己在 Makefile 中为每个文件指定规则。

## 配置变量

在 Makefile 的第一部分中，有几个变量可以进行配置：

- `DIR_SRC`：源文件目录的名称。
- `DIR_INC`：头文件目录的名称。
- `DIR_OBJ`：对象文件目录的名称。
- `COMPILER`：您要使用的编译器。
- `EXT`：源文件使用的扩展名。
- `TARGET`：目标可执行文件的名称。
- `COMMONFLAGS`：通用编译器标志。
- `CFLAGS`：C 编译器标志。
- `CXXFLAGS`：C++ 编译器标志。
- `COMMONLIBS`：通用库链接器标志。
- `WIN32LIBS`：适用于 Windows 的库链接器标志。
- `LINUXLIBS`：适用于 Linux 的库链接器标志。

## 使用方法

1. **初始化目录**：
   ```bash
   make init
   ```
   该命令将创建源文件、头文件和对象文件目录。

2. **构建目标**：
   ```bash
   make
   ```
   该命令将构建目标可执行文件。

## 注意事项

- 确保您的源文件和头文件分别放置在 `DIR_SRC` 和 `DIR_INC` 目录中。
- 根据您的项目需求，调整 Makefile 中的配置变量。

通过这个简单的 Makefile，您可以更轻松地管理和构建您的 C 和 C++ 项目。

## 下载链接

[C和C项目的简单Makefile](https://pan.quark.cn/s/7969578c0bee)