---
layout: post
title: "Ubuntu 离线安装包：gcc、make、build-essential 及依赖"
date:   2022-09-30
tags: [essential,build,gcc,make,deb]
comments: true
author: admin
---
# Ubuntu 离线安装包：gcc、make、build-essential 及依赖

## 简介

本仓库提供了一个离线安装包，包含了在 Ubuntu 系统上安装 `gcc`、`make` 和 `build-essential` 所需的 `.deb` 文件及其依赖项。这些资源适用于在没有网络连接的环境中安装基本的编译环境。

## 资源文件

- **文件名**: `gcc、make、build-essential离线安装包及依赖.zip`
- **内容**: 
  - `gcc` 目录：包含 `gcc` 的 `.deb` 文件及其 12 个依赖项。
  - `make` 目录：包含 `make` 的 `.deb` 文件及其 1 个依赖项。
  - `build-essential` 目录：包含 `build-essential` 的 `.deb` 文件及其 7 个依赖项（不包括 `build-essential` 本身）。

## 安装步骤

1. 将 `gcc、make、build-essential离线安装包及依赖.zip` 文件拷贝到目标离线电脑上并解压。
2. 依次进入解压后的目录：
   - 首先进入 `gcc` 目录，执行以下命令安装 `gcc` 及其依赖：
     ```bash
     cd gcc
     sudo dpkg -i *.deb
     ```
   - 然后进入 `make` 目录，执行以下命令安装 `make` 及其依赖：
     ```bash
     cd ../make
     sudo dpkg -i *.deb
     ```
   - 最后进入 `build-essential` 目录，执行以下命令安装 `build-essential` 及其依赖：
     ```bash
     cd ../build-essential
     sudo dpkg -i *.deb
     ```

## 注意事项

- 请务必按照 `gcc`、`make`、`build-essential` 的顺序进行安装，否则可能会导致安装失败。
- 如果在安装过程中遇到依赖问题，可以尝试使用 `sudo apt-get install -f` 命令来修复依赖关系。

## 贡献

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交 Issue 或 Pull Request。

## 许可证

本仓库中的资源文件遵循其原始许可证。具体许可证信息请参考每个 `.deb` 文件的原始来源。

## 下载链接

[Ubuntu离线安装包gccmakebuild-essential及依赖](https://pan.quark.cn/s/3e7a232841cc)