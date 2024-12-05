---
layout: post
title: "Win10 Anaconda 新建环境安装pythonpcl"
date:   2020-04-13
tags: [pcl,python,Anaconda,Python,安装]
comments: true
author: admin
---
# Win10 Anaconda 新建环境安装python-pcl

本文详细介绍了在Windows 10系统下，使用Anaconda创建新环境并安装python-pcl库的步骤。python-pcl是一个用于处理点云数据的Python库，广泛应用于计算机视觉和机器人领域。

## 一、前言

在Windows环境下安装pcl库可能会遇到一些挑战，尤其是在使用Anaconda管理Python环境时。本文将指导你如何通过Anaconda创建虚拟环境，并在此环境中安装python-pcl库。

## 二、安装流程

### 1. 创建Anaconda虚拟环境

首先，使用Anaconda创建一个新的虚拟环境，并指定Python版本。例如，创建一个名为`pytorch_pcl`的环境，并设置Python版本为3.7：

```bash
conda create -n pytorch_pcl python=3.7
```

如果你需要使用Python 3.6版本，可以相应地修改命令：

```bash
conda create -n pytorch_pcl python=3.6
```

### 2. 下载python-pcl的whl文件

python-pcl库的编译版本可以在以下网盘地址中找到：

- Python 3.7版本：提取码 pcl3
- Python 3.6版本：提取码 rphc

你也可以直接从PyPI下载合适的python-pcl版本，无需一定要在网盘下载。

### 3. 安装python-pcl

将下载到的`python_pcl-0.3.0rc1-cp37-cp37m-win_amd64.whl`文件放入所创建的虚拟环境的`Scripts`文件夹下，例如：

```
D:\Anaconda3\Scripts
```

然后，在此文件夹下打开命令提示符，执行以下命令进行安装：

```bash
pip install python_pcl-0.3.0rc1-cp37-cp37m-win_amd64.whl
```

或者，你也可以在Anaconda Prompt下运行以下命令：

```bash
conda create -n python_pcl_37 python=3.7
activate python_pcl_37
pip install python_pcl-0.3.0rc1-cp37-cp37m-win_amd64.whl
```

### 4. 解决DLL加载失败问题

在安装完成后，导入`pcl`模块时可能会遇到以下错误：

```
ImportError: DLL load failed: 找不到指定的模块
```

这是因为pcl库依赖于OpenNI2的dll文件。你需要从OpenNI官网下载并安装OpenNI2，然后将`OpenNI2.dll`文件复制到Anaconda环境的`site-packages\pcl`目录下。

## 三、结语

通过以上步骤，你应该能够在Windows 10系统下成功安装并使用python-pcl库。如果在安装过程中遇到任何问题，欢迎参考本文提供的解决方案或留言讨论。

## 下载链接

[Win10Anaconda新建环境安装python-pcl分享](https://pan.quark.cn/s/7407b5d04d6d)