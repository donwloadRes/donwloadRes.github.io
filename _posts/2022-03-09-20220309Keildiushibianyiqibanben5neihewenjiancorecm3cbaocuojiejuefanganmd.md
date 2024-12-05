---
layout: post
title: "Keil 丢失编译器版本5内核文件corecm3c报错解决方案"
date:   2024-09-22
tags: [编译器,core,cm3,Keil,文件]
comments: true
author: admin
---
# Keil 丢失编译器版本5、内核文件core_cm3.c报错解决方案

## 简介

本资源文件旨在解决在使用Keil开发工具时遇到的“丢失编译器版本5”和“内核文件core_cm3.c报错”的问题。这些问题通常出现在使用较新版本的Keil编译器时，尤其是从编译器版本6开始，旧版本的core_cm3.c文件可能不再兼容。

## 问题描述

在使用Keil进行嵌入式开发时，可能会遇到以下错误：
1. **Missing Compiler Version 5**: 编译器无法找到版本5的相关文件。
2. **core_cm3.c报错**: 在编译过程中，core_cm3.c文件出现错误，导致编译失败。

## 解决方案

### 1. 下载并安装ARM Compiler 5

首先，需要下载并安装ARM Compiler 5。可以从以下链接下载：
- 下载链接：[百度网盘](请输入提取码)
- 提取码：zv2i

下载完成后，解压文件并将ARMCC文件夹复制到Keil安装目录下的ARM目录中。

### 2. Keil配置

1. 打开Keil软件。
2. 进入`Folders/Extensions`选项。
3. 添加ARMCC文件夹。
4. 选择版本5作为编译器。

### 3. 更新内核文件

如果仍然遇到core_cm3.c文件的报错，可以尝试以下方法：

#### 方法一：更换编译器版本

在Target选项中，选择使用编译器版本5进行编译。

#### 方法二：更新相关内核文件

1. 打开安装MDK的目录：`F:\KEIL_C51\ARM\CMSIS\5.9.0\CMSIS\Core\Include`。
2. 复制以下4个文件：
   - core_cm3.h
   - cmsis_version.h
   - cmsis_compiler.h
   - cmsis_armclang.h
3. 将这些文件粘贴到项目工程的启动文件夹中，例如`Startup`文件夹。
4. 确保在Target中包含这些文件的路径。

## 总结

通过以上步骤，可以有效解决Keil丢失编译器版本5和core_cm3.c报错的问题。如果使用旧版本的core_cm3.c文件，建议使用编译器版本5进行编译；如果希望使用编译器版本6，则需要更新相关的内核文件。

## 下载链接

[Keil丢失编译器版本5内核文件core_cm3.c报错解决方案](https://pan.quark.cn/s/49ca6e4ec5d7)