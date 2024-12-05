---
layout: post
title: "FortifySCA 扫描工具指导手册"
date:   2020-11-24
tags: [Fortify,SCA,扫描,手册,阶段]
comments: true
author: admin
---
# Fortify-SCA 扫描工具指导手册

## 简介

本仓库提供了一份名为“Fortify-SCA-扫描工具指导手册.pdf”的资源文件，该文件详细介绍了Fortify SCA扫描工具的使用方法和操作步骤。手册内容涵盖了Fortify SCA的分析原理、扫描过程、命令行参数说明以及源代码转换等内容，对实际工作具有重要的指导作用。

## 资源文件描述

- **文件名**: Fortify-SCA-扫描工具指导手册.pdf
- **文件类型**: PDF
- **文件大小**: [文件大小]
- **下载链接**: [下载链接]

## 内容概述

### Fortify SCA 分析原理

- **Front-End**: 3rd party IDE, Java Plug-In, C/C++ MicrosoLNET, IBM Eclipse
- **Audit Workbench**: PLSQL, XML
- **Analysis Engine**: Semantic, fdi/fpr, Global Data flow, Control Flow, Configuration, Structural
- **Fortify Manager**: Rules Builder, Custom Pre-Packaged

### Fortify SCA 分析过程

- **阶段一: 转换阶段 (Translation)**
- **阶段二: 分析阶段 (Scan)**
- **阶段三: 查看阶段 (Show-fe)**
- **阶段四: 扫描阶段 (Scan)**

### Fortify SCA 扫描的工作

- **Visual Studio**
- **Eclipse**
- **IBM RAD**
- **Audit Workbench**
- **Java, .NET, C/C++**
- **Analysis, JSP, Touchless Build**
- **PL/SQL, IDE, Intermediate, FPR, TSQL, Model, Cold Command Line Interface**

### Fortify SCA 扫描的五种方式

- **插件方式: Plug-In (Eclipse, VS, WSAD, RAD)**
- **命令行方式: Command line**
- **扫描目录方式: Audit Workbench scan Folder**
- **与其他工具集成: Scan with ANT, Makefile**
- **编译监控器方式: Fortify SCA Build Monitor**

### Fortify SCA 扫描的四个步骤

1. **Clean: 清除阶段**
2. **Translation: 转换阶段**
3. **Show-fe: 查看阶段**
4. **Scan: 扫描阶段**

### Fortify SCA 命令行参数说明

- **查看SCA扫描命令及参数**: `sourceanalyzer --help`
- **常用命令**: `sourceanalyzer -b <buildid> <files>`
- **输出选项**: `-format <fmt>`, `-f <file>`, `build-project <name>`, `build-label <label>`, `build-version <version>`

### Fortify SCA 转换源代码

- **Java代码转换**
- **J2EE应用程序转换**
- **.NET源代码转换**
- **C/C++代码转换**
- **PL/SQL转换**

## 使用说明

1. **下载文件**: 点击下载链接，获取“Fortify-SCA-扫描工具指导手册.pdf”文件。
2. **阅读手册**: 打开PDF文件，按照手册中的步骤进行操作。
3. **实践操作**: 根据手册中的指导，进行Fortify SCA扫描工具的实际操作。

## 注意事项

- 请确保在操作前已经安装了Fortify SCA工具。
- 手册中的命令行参数和步骤可能需要根据实际情况进行调整。
- 如果在操作过程中遇到问题，请参考手册中的常见问题解答部分。

## 贡献

如果您在使用过程中发现任何问题或有改进建议，欢迎提交Issue或Pull Request。

## 许可证

本资源文件遵循[许可证名称]许可证。详细信息请参阅LICENSE文件。

## 下载链接

[Fortify-SCA扫描工具指导手册](https://pan.quark.cn/s/67a3db0cd299)