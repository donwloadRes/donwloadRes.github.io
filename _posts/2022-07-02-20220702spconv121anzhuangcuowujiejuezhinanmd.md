---
layout: post
title: "spconv1.2.1安装错误解决指南"
date:   2022-01-30
tags: [spconv1.2,安装,版本,解决方案,subprocess]
comments: true
author: admin
---
# spconv1.2.1安装错误解决指南

本文档旨在帮助用户解决在安装spconv1.2.1过程中遇到的`subprocess.CalledProcessError`错误。通过详细的步骤和解决方案，用户可以顺利完成spconv1.2.1的安装。

## 错误描述

在执行`python setup.py bdist_wheel`命令时，可能会遇到以下错误：

```
subprocess.CalledProcessError: Command '['cmake', '--build', ' ', '--config', 'Release', '--', '-j4']' returned non-zero exit status 2
```

## 可能原因及解决方案

### 1. pybind11文件缺失

**问题描述**：从官方下载的spconv1.2.1文件夹下的`third_party/pybind11`目录为空。

**解决方案**：手动下载pybind11文件并放置在`third_party/pybind11`目录下。

### 2. CUDA版本与GPU架构不匹配

**问题描述**：使用30系列显卡时，需要安装CUDA11.x版本，而spconv需要安装2.x版本。

**解决方案**：确保CUDA版本与GPU架构匹配，并设置正确的CUDA环境变量。

### 3. gcc版本错误导致的编译失败

**问题描述**：gcc版本不兼容导致编译失败。

**解决方案**：更新gcc版本至兼容版本。

### 4. 30系列显卡的CUDA支持问题

**问题描述**：nvcc报错`Unsupported gpu architecture 'compute_89'`。

**解决方案**：设置环境变量`TORCH_CUDA_ARCH_LIST="8.0"`并重新编译。

### 5. 其他可能的解决方案

- 删除`/spconv/build/`文件夹中的所有内容，重新安装。
- 创建新的conda环境并重新安装spconv。

## 总结

通过以上步骤，用户可以有效解决spconv1.2.1安装过程中遇到的`subprocess.CalledProcessError`错误，确保安装顺利完成。

## 下载链接

[spconv1.2.1安装错误解决指南](https://pan.quark.cn/s/6a5474782226)