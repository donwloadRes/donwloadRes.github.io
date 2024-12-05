---
layout: post
title: "零基础入门国产数据库资源dmPython安装详解"
date:   2021-01-18
tags: [dmPython,安装,数据库,环境变量,python]
comments: true
author: admin
---
# 零基础入门：国产数据库资源dmPython安装详解

本指南旨在为初学者提供一个详细的教程，帮助他们在 Windows 和 Linux 环境下安装和使用国产数据库资源 dmPython，避免常见的安装陷阱。

## 内容概述

1. **Windows 环境下的 dmPython 安装**
   - 使用 Anaconda 创建虚拟环境
   - 下载并安装 dmPython
   - 配置环境变量和依赖文件

2. **Linux 环境下的 dmPython 安装**
   - 内置数据库资源版本的安装
   - 无内置数据库资源版本的安装
   - 配置环境变量和依赖文件

3. **常见问题及解决方法**

## 安装步骤

### Windows 环境

1. **创建虚拟环境**
   - 使用 Anaconda Prompt，创建一个新的 conda 环境：`conda create -n dmPython --clone base`
   - 激活环境：`conda activate dmPython`

2. **下载并安装 dmPython**
   - 导航到 dmPython 安装目录：`cd D:\DM\dmdbs\drivers\python\dmPython`
   - 执行安装命令：`python setup.py install`

3. **配置环境变量和依赖文件**
   - 复制 dpi 文件夹中的所有 dll 文件到 dmPython 的安装目录。
   - 将 libeay32.dll 和 ssleay32.dll 文件复制到当前虚拟环境中的 python.exe 所在目录。

### Linux 环境

1. **内置数据库资源版本的安装**
   - 配置环境变量：`vi ~/.bash_profile`
   - 导航到驱动安装路径：`cd /data/soft/dmdba/dmdbms/drivers/python/dmPython/`
   - 执行安装命令：`python setup.py install`

2. **无内置数据库资源版本的安装**
   - 从具有已安装数据库资源的计算机导出相关目录并解压。
   - 配置环境变量：`vim ~/.bash_profile`
   - 导航到解压后的目录并执行安装命令：`python setup.py install`

## 排错技巧

- **安装过程中报错**：这通常是由于缺少依赖文件或环境变量配置不当。仔细检查所有所需的 dll 文件和环境变量，确保其已正确设置。
- **无法导入 dmPython 模块**：确保所有依赖文件已正确复制到相应的目录，然后重试导入。

通过遵循本指南，您应该能够在 Windows 和 Linux 系统中轻松安装和配置 dmPython，从而使用 Python 与国产数据库资源进行交互。

## 下载链接

[0基础学挨踢-国产达梦数据库dmPython安装和避坑](https://pan.quark.cn/s/75d7d02a199b)