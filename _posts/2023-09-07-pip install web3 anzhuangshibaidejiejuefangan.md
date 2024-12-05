---
layout: post
title: "pip install web3 安装失败的解决方案"
date:   2021-07-13
tags: [web3,pip,安装,install,https]
comments: true
author: admin
---
# pip install web3 安装失败的解决方案

## 简介

本仓库提供了一个资源文件，详细记录了在安装 `web3` 库时遇到的种种问题及其解决方案。文章标题为“pip install web3 一直失败！！！（超级无敌血泪史）”，原文可以在 [CSDN博客](https://blog.csdn.net/zeroheitao/article/details/115134616) 上找到。

## 问题描述

在尝试使用 `pip install web3` 命令安装 `web3` 库时，可能会遇到以下错误：

- 缺少 `bitarray`、`lru-dict`、`cytoolz` 等依赖库。
- 安装过程中出现 `Building wheel for bitarray (setup.py): started` 等错误信息。
- 提示需要 Microsoft Visual C++ 14.0 或更高版本。

## 解决方案

### 1. 安装 Microsoft Visual C++ Build Tools

由于 `web3` 库及其依赖项需要编译，因此需要安装 Microsoft Visual C++ Build Tools。可以从 [Microsoft 官方网站](https://visualstudio.microsoft.com/visual-cpp-build-tools/) 下载并安装。

### 2. 手动安装缺失的依赖库

如果 `pip install web3` 失败，可以尝试手动安装缺失的依赖库：

1. 下载缺失库的 `.whl` 文件，可以从 [Unofficial Windows Binaries for Python Extension Packages](https://www.lfd.uci.edu/~gohlke/pythonlibs/) 网站获取。
2. 使用 `pip install <filename>.whl` 命令安装下载的 `.whl` 文件。

### 3. 使用国内镜像源

有时由于网络问题，`pip` 安装可能会失败。可以尝试使用国内的镜像源来加速安装：

```bash
pip install web3 -i https://pypi.tuna.tsinghua.edu.cn/simple
```

### 4. 其他注意事项

- 确保 Python 环境配置正确，且没有多个 Python 版本冲突。
- 如果使用虚拟环境，确保激活虚拟环境后再进行安装。

## 总结

通过以上步骤，应该能够成功安装 `web3` 库及其依赖项。如果仍有问题，请参考原文中的详细描述和解决方案。

---

希望这个 README 文件能帮助你顺利解决 `pip install web3` 的问题！

## 下载链接

[pipinstallweb3安装失败的解决方案](https://pan.quark.cn/s/150a2c6d8b22)