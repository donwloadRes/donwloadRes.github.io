---
layout: post
title: "Keil5 报错记录Missing Compiler Version 5 解决方案"
date:   2022-04-30
tags: [Keil5,Compiler,Version,ARM,编译器]
comments: true
author: admin
---
# Keil5 报错记录：Missing Compiler Version 5 解决方案

## 简介

本资源文件旨在帮助解决在使用Keil5开发环境时遇到的“Missing Compiler Version 5”报错问题。该问题通常出现在使用较新版本的Keil5时，由于默认未安装ARM Compiler Version 5编译器而导致的编译错误。

## 问题描述

在使用Keil5进行嵌入式开发时，可能会遇到以下报错信息：

```
missing compiler kueil5
```

这通常是因为Keil5默认没有安装ARM Compiler Version 5编译器，而某些旧版本的工程文件需要使用该编译器进行编译。

## 解决方案

### 1. 检查认证

首先，确保你的Keil5已经正确认证，并且没有认证问题。

### 2. 安装ARM Compiler Version 5

如果你下载的是5.37版本或更高版本的Keil5，默认情况下是没有ARM Compiler Version 5编译器的。你需要自行下载并安装该编译器。

#### 下载方式

- **官网下载**：从ARM官网下载ARM Compiler Version 5编译器。
- **百度网盘下载**：提供百度网盘下载链接，提取码为：4c3c。

### 3. 配置编译器路径

安装完成后，需要将ARM Compiler Version 5的路径添加到Keil5的编译器路径中。

1. 打开Keil5，点击“魔法棒”图标右侧的三个小方块。
2. 在弹出的窗口中，添加ARM Compiler Version 5的安装目录，例如：
   ```
   C:\Keil_v5\ARM\ARM_Compiler_5.06u7
   ```
3. 确认路径添加成功后，重新编译工程。

## 注意事项

- 确保ARM Compiler Version 5的安装路径正确无误。
- 如果仍然遇到问题，请检查是否存在其他配置错误或环境变量设置问题。

## 结语

通过以上步骤，你应该能够成功解决Keil5中的“Missing Compiler Version 5”报错问题。如果仍有疑问，欢迎在评论区留言讨论。

## 下载链接

[Keil5报错记录MissingCompilerVersion5解决方案](https://pan.quark.cn/s/24f9fd1c0da1)