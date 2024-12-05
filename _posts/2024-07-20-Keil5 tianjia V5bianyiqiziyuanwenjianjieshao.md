---
layout: post
title: "Keil5 添加 V5编译器资源文件介绍"
date:   2020-03-29
tags: [编译器,Version,ARM,版本,Compiler]
comments: true
author: admin
---
# Keil5 添加 V5编译器资源文件介绍

本资源文件旨在帮助用户在Keil5开发环境中添加V5编译器，以解决编译器版本不匹配的问题。以下是详细的步骤和说明。

## 问题描述

在更新最新的Keil版本（MDK5.37）后，用户在编译以前版本的工程文件时，可能会遇到编译器版本不匹配的问题。具体表现为MDK5.37中使用的是Version 6版本的编译器，而缺少Version 5。对于以前编写的工程文件来说，需要使用的是Version 5版本，因此产生了报错。

## 解决方案

重新下载ARM Compiler Version 5编译器即可解决此问题。以下是详细步骤：

### 1. 下载ARM Compiler Version 5

用户需要下载ARM Compiler Version 5版本的编译器ARMCC。下载完成后，解压文件。

### 2. 复制到Keil安装目录

将解压后的文件复制到Keil安装目录下的ARM文件夹中。

### 3. 配置Keil

1. 打开Keil，进入`File Extension, Books and Environment`。
2. 选择`Folders/Extensions`，点击`Use ARM Compiler`方框中的选项。
3. 选择`Add another ARM Compiler Version to List`，找到并添加刚刚下载好的文件ARMCC。

### 4. 验证配置

再次打开`Options`选项，确认Version 5的编译器已经安装好。

## 注意事项

- 确保下载的ARM Compiler Version 5版本与Keil版本兼容。
- 在配置过程中，如果遇到路径问题，可以通过`Add another ARM Compiler Version to List`选项自动打开对应路径，并将ARMCC复制到对应路径下。

通过以上步骤，用户可以在Keil5中成功添加V5编译器，解决编译器版本不匹配的问题。

## 下载链接

[Keil5添加V5编译器资源文件介绍](https://pan.quark.cn/s/815eb03c04c1)