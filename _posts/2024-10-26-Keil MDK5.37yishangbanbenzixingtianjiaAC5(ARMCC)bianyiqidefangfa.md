---
layout: post
title: "Keil MDK5.37以上版本自行添加AC5(ARMCC)编译器的方法"
date:   2023-06-17
tags: [编译器,Keil,AC5,ARMCC,MDK5.37]
comments: true
author: admin
---
# Keil MDK5.37以上版本自行添加AC5(ARMCC)编译器的方法

本仓库提供了一个详细的教程和资源文件，帮助用户在Keil MDK5.37及以上版本中自行添加AC5（ARMCC）编译器。

## 内容概述

- **教程来源**：本教程基于CSDN博客文章《Keil MDK5.37以上版本自行添加AC5(ARMCC)编译器的方法》。
- **主要步骤**：
  1. 下载AC5(ARMCC)编译器。
  2. 安装编译器到指定路径。
  3. 在Keil MDK中设置编译器路径。
  4. 验证编译器是否成功添加。

## 使用说明

1. **下载编译器**：
   - 从官方页面或提供的网盘链接下载AC5(ARMCC)编译器。

2. **安装编译器**：
   - 将下载的编译器安装到Keil安装目录下的ARM文件夹中，新建一个名为ARMCC的文件夹。
   - 注意：安装路径不要包含特殊字符，否则可能导致编译错误。

3. **设置编译器路径**：
   - 打开Keil MDK，切换至`Folders/Extensions`选项卡。
   - 点击`Use Arm Complier`一栏最后的三个点，选择刚刚安装的编译器路径。

4. **验证编译器**：
   - 在`Options`的`Target`选项卡中，查看可选编译器，确认`Use default compiler 5`（即AC5）是否出现。

## 注意事项

- 确保安装路径不包含特殊字符，避免编译错误。
- 如果遇到编译时提示找不到序列号的错误，请参考原文中的解决方法。

## 参考资料

- 本教程基于CSDN博客文章《Keil MDK5.37以上版本自行添加AC5(ARMCC)编译器的方法》，详细步骤和解决方案请参考该文章。

---

通过本教程和资源文件，您可以顺利在Keil MDK5.37及以上版本中添加AC5(ARMCC)编译器，提升开发效率。

## 下载链接

[KeilMDK5.37以上版本自行添加AC5ARMCC编译器的方法](https://pan.quark.cn/s/e7af735196d7)