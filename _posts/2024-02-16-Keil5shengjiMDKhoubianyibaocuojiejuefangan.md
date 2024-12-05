---
layout: post
title: "Keil5升级MDK后编译报错解决方案"
date:   2020-10-12
tags: [Compiler,ARM,编译,Keil5,Target]
comments: true
author: admin
---
# Keil5升级MDK后编译报错解决方案

## 简介

本资源文件旨在帮助解决Keil5升级到MDK后编译报错的问题。随着Keil5的升级，许多用户在编译项目时遇到了各种错误，尤其是在使用旧版本的编译器时。本文将提供详细的解决方案，帮助用户顺利完成编译。

## 问题描述

在Keil5升级到MDK后，许多用户在编译项目时遇到了以下错误：

```
*** Target 'Target 1' uses ARM-Compiler 'Default Compiler Version 5' which is not available.
*** Please review the installed ARM Compiler Versions: 'Manage Project Items - Folders/Extensions' to manage ARM Compiler Versions.
*** 'Options for Target - Target' to select an ARM Compiler Version for the target.
*** Build aborted.
```

## 解决方案

### 1. 安装ARM Compiler Version 5

由于MDK5.37及以上的版本默认不再安装ARM Compiler Version 5，因此需要手动安装该编译器。可以从之前版本的Keil安装目录中找到`ARMCC`文件夹，并将其复制到新版本的Keil安装目录中。

### 2. 配置Keil项目

在Keil中打开项目，进入`Manage Project Items - Folders/Extensions`，添加ARM Compiler Version 5。然后在`Options for Target - Target`中选择ARM Compiler Version 5作为目标编译器。

### 3. 重新编译项目

完成上述配置后，重新编译项目，应该可以解决编译报错的问题。

## 注意事项

- 确保从可靠的来源获取ARM Compiler Version 5文件。
- 在复制文件时，注意备份原有文件，以防出现意外情况。

## 总结

通过以上步骤，用户可以顺利解决Keil5升级MDK后编译报错的问题。希望本资源文件能够帮助到遇到类似问题的开发者。

## 下载链接

[Keil5升级MDK后编译报错解决方案](https://pan.quark.cn/s/c981f23424a1)