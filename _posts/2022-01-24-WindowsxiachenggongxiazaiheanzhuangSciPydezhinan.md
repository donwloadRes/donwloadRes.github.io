---
layout: post
title: "Windows下成功下载和安装SciPy的指南"
date:   2023-01-10
tags: [安装,SciPy,NumPy,pip,MKL]
comments: true
author: admin
---
# Windows下成功下载和安装SciPy的指南

本文将详细介绍如何在Windows系统中成功下载和安装SciPy，并包含NumPy+MKL的安装步骤和百度网盘资源的下载方法。

## 1. 准备工作

在开始之前，请确保你已经安装了Python，并且使用的是PyCharm作为IDE。如果你使用的是Anaconda，那么很多科学计算库已经集成在内，不需要单独安装。

## 2. 安装NumPy+MKL

SciPy依赖于NumPy+MKL，因此在安装SciPy之前，必须先安装NumPy+MKL。

### 2.1 卸载已有的NumPy

在PyCharm中，打开Terminal，输入以下命令查看已安装的扩展包：
```
pip list
```
如果已经安装了NumPy，请使用以下命令卸载：
```
pip uninstall numpy
```

### 2.2 确定安装包版本

在Python Console中输入以下代码，查看你的电脑兼容的安装包版本：
```python
import pip._internal.pep425tags
print(pip._internal.pep425tags.get_supported())
```
输出结果将显示你的Python版本和系统架构，例如`cp37-cp37m-win32`表示Python 3.7版本，32位系统。

### 2.3 下载NumPy+MKL

从百度网盘下载适合你系统的NumPy+MKL安装包，并将其放置在项目的Scripts文件夹中。然后在Terminal中输入以下命令进行安装：
```
pip install 路径\numpy-1.17.2+mkl-cp37-none-win32.whl
```
安装成功后，可以在项目路径中看到新增的NumPy包。

## 3. 安装SciPy

### 3.1 下载SciPy

从百度网盘下载适合你系统的SciPy安装包，并将其放置在项目的Scripts文件夹中。然后在Terminal中输入以下命令进行安装：
```
pip install 路径\scipy-1.4.1-cp37-cp37m-win32.whl
```
安装成功后，可以在Python Console中输入以下代码检查是否安装成功：
```python
import numpy
import scipy
```
如果没有报错，说明安装成功。

## 4. 总结

通过以上步骤，你可以在Windows系统中成功下载和安装SciPy，并确保NumPy+MKL的正确安装。希望本文对你有所帮助！

## 下载链接

[Windows下成功下载和安装SciPy的指南分享](https://pan.quark.cn/s/402b529d4d0a)