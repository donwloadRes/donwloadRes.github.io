---
layout: post
title: "Ubuntu-Kylin 系统离线安装 GCC、G++、C++ 资源文件"
date:   2024-07-27
tags: [文件,安装,资源,8.4,离线]
comments: true
author: admin
---
# Ubuntu/Kylin 系统离线安装 GCC、G++、C++ 资源文件

## 描述

本仓库提供了一个用于在 Ubuntu 或 Kylin 系统上离线安装 GCC、G++ 和 C++ 编译器的资源文件。该资源文件包含了所有必要的依赖包，确保您可以在没有网络连接的情况下完成安装。

## 包含的包

以下是资源文件中包含的所有包及其版本：

- `binutils-common`
- `binutils-x86-64-linux-gnu`
- `binutils`
- `cpp-7`
- `g++-7`
- `gcc-7-base`
- `gcc-7`
- `gcc-8-base`
- `libasan4`
- `libatomic1`
- `libbinutils`
- `libc-bin`
- `libc-dev-bin`
- `libc6-dev`
- `libc6`
- `libcc1`
- `libcilkrts5`
- `libgcc-7`
- `libgcc1`
- `libgomp1`
- `libisl1`
- `libitm1`
- `liblsan0_8.4.0-1`
- `libmpc3_1.1.0-1_amd64.deb`
- `libmpfr6_4.0.1-1_amd64.deb`
- `libmpx2_8.4.0-1`
- `libquadmath0_8.4.0-1`
- `libstdc++-7-dev_7.5.0-3`
- `libstdc++6_8.4.0-1`
- `libtsan0_8.4.0-1`
- `libubsan0_7.5.0-3`
- `linux-libc-dev_4.15.0-103.104_amd64.deb`
- `locales_2.27-3`

## 使用方法

1. **下载资源文件**：
   从本仓库下载包含所有依赖包的资源文件。

2. **解压文件**：
   将下载的资源文件解压到您的系统中。

3. **安装依赖包**：
   在终端中进入解压后的目录，并运行以下命令来安装所有依赖包：

   ```bash
   sudo dpkg -i *.deb
   ```

4. **完成安装**：
   安装完成后，您可以使用 `gcc`、`g++` 和 `c++` 命令来编译您的代码。

## 注意事项

- 请确保您的系统架构与资源文件中的包架构一致（例如，本资源文件适用于 `amd64` 架构）。
- 如果在安装过程中遇到依赖问题，您可以尝试使用 `apt-get install -f` 命令来解决依赖关系。

## 贡献

如果您发现任何问题或有改进建议，欢迎提交 Issue 或 Pull Request。

## 许可证

本仓库中的资源文件遵循其原始许可证。请参考每个包的许可证信息。

---

希望这个资源文件能够帮助您顺利完成 GCC、G++ 和 C++ 的离线安装！

## 下载链接

[UbuntuKylin系统离线安装GCCGC资源文件](https://pan.quark.cn/s/7b0de91c72d0)