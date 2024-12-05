---
layout: post
title: "解决ARMCompiler Default Compiler Version 5不可用问题"
date:   2022-12-05
tags: [Compiler,ARM,编译器,Version,MDK]
comments: true
author: admin
---
# 解决ARM-Compiler 'Default Compiler Version 5'不可用问题

## 简介
本仓库提供了一个资源文件，用于解决在使用ARM-Compiler时遇到的“Default Compiler Version 5不可用”的问题。该问题通常出现在新版MDK（Microcontroller Development Kit）中，由于新版MDK不再包含ARM-Compiler Version 5，导致旧工程无法编译。

## 问题描述
在使用新版MDK编译旧工程时，可能会遇到以下错误提示：
```
Target 'XXX' uses ARM-Compiler 'Default Compiler Version 5' which is not available
```
这是因为新版MDK不再自带ARM-Compiler Version 5编译器，导致旧工程无法正常编译。

## 解决方案
为了解决这个问题，用户需要手动下载并安装ARM-Compiler Version 5的最后一版编译器，并在MDK设置中指定该编译器的路径。

### 步骤
1. **下载ARM-Compiler Version 5编译器**：
   - 本仓库提供的资源文件即为ARM-Compiler Version 5的最后一版编译器。

2. **安装编译器**：
   - 解压下载的资源文件，并运行其中的安装程序。

3. **在MDK中指定编译器路径**：
   - 打开MDK，进入工程设置，找到“Folders/Extensions”选项。
   - 在“ARM Compiler”部分，指定刚刚安装的ARM-Compiler Version 5的路径。

4. **重新编译工程**：
   - 完成上述设置后，重新编译工程，错误提示应消失，工程应能正常编译。

## 注意事项
- 确保下载的编译器版本与工程所需的版本一致。
- 安装编译器后，务必在MDK中正确指定编译器路径，否则仍会遇到编译错误。

## 支持与反馈
如果在使用过程中遇到任何问题，欢迎在仓库中提交Issue，我们会尽快回复并提供帮助。

---

通过以上步骤，您应该能够成功解决ARM-Compiler 'Default Compiler Version 5'不可用的问题，确保旧工程能够在新版MDK中正常编译。

## 下载链接

[解决ARM-CompilerDefaultCompilerVersion5不可用问题](https://pan.quark.cn/s/46b5c004ebeb)