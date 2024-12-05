---
layout: post
title: "GCC Linaro 7.3.1 交叉编译工具链"
date:   2023-08-28
tags: [解压,编译,工具,7.3,x86]
comments: true
author: admin
---
# GCC Linaro 7.3.1 交叉编译工具链

## 资源文件

**文件名**: `gcc-linaro-7.3.1-2018.05-x86_64_aarch64-linux-gnu.tar.xz`

## 描述

该资源文件是一个用于交叉编译Linux内核的工具链。它包含了Linaro GCC 7.3.1版本，适用于x86_64架构的系统，并能够生成aarch64架构的二进制文件。该工具链特别适用于Jetson板子的开发和编译工作。

## 使用说明

1. **下载文件**: 下载本仓库中的`gcc-linaro-7.3.1-2018.05-x86_64_aarch64-linux-gnu.tar.xz`文件。

2. **解压文件**: 使用7z格式解压工具（如7-Zip）进行解压。解压后会得到一个包含工具链的目录。

3. **设置环境变量**: 将解压后的工具链路径添加到系统的`PATH`环境变量中，以便在命令行中可以直接调用该工具链。

4. **交叉编译**: 使用该工具链进行Linux内核的交叉编译。具体编译步骤请参考相关文档或教程。

## 注意事项

- 请确保系统中已安装7z解压工具，以便正确解压文件。
- 在使用该工具链进行编译时，请确保目标系统与Jetson板子的架构一致。

## 版本信息

- **Linaro GCC**: 7.3.1
- **发布日期**: 2018.05
- **架构**: x86_64 (主机) / aarch64 (目标)

## 支持与反馈

如有任何问题或建议，请在仓库中提交Issue，我们会尽快回复并提供帮助。

## 下载链接

[GCCLinaro7.3.1交叉编译工具链](https://pan.quark.cn/s/1d81da8eba2c)