---
layout: post
title: "树莓派4B安装Pytorch新版本13Python 37"
date:   2024-03-23
tags: [树莓,Pytorch,安装,1.3,4B]
comments: true
author: admin
---
# 树莓派4B+安装Pytorch新版本1.3（Python 3.7）

## 简介

本资源文件提供了在树莓派4B+上安装Pytorch新版本1.3（Python 3.7）的详细步骤和所需文件。Pytorch是一个强大的深度学习框架，适用于构建神经网络模型。树莓派是一款流行的开源硬件平台，通常用于教育、实验和小型项目。通过本资源，您可以轻松地在树莓派4B+上部署Pytorch，进行神经网络相关的任务。

## 背景

最近，越来越多的开发者需要在树莓派上部署神经网络相关的任务。为了在树莓派上安装Pytorch，许多开发者参考了各种文章和教程。然而，直接通过pip安装新版本的Pytorch在树莓派上并不容易实现，通常需要编译安装。本资源文件分享了已经编译好的Pytorch 1.3版本，针对Python 3.7，帮助开发者免去复杂的编译过程，直接安装使用。

## 安装步骤

1. **安装必要的依赖包**
   ```bash
   sudo apt-get install libopenblas-dev
   ```

2. **安装numpy和pyyaml**
   ```bash
   pip3 install numpy pyyaml
   ```

3. **安装Pytorch**
   ```bash
   pip3 install torch-1.3.0a0+de394b6-cp37-cp37m-linux_armv7l.whl
   ```

4. **安装torchvision**
   ```bash
   pip3 install torchvision-0.4.1a0+a263704-cp37-cp37m-linux_armv7l.whl
   ```

## 注意事项

- 确保树莓派的操作系统和Python版本与本资源文件中的配置一致。
- 如果在安装过程中遇到问题，请参考原始文章中的详细步骤和解决方案。

## 参考文章

本资源文件的安装步骤和详细说明参考了以下文章：
- [树莓派（7）：树莓派4B+安装Pytorch新版本1.3（python3.7）](https://blog.csdn.net/zhaodongyu_ak47/article/details/105055856)

通过本资源文件，您可以轻松地在树莓派4B+上安装Pytorch 1.3版本，开始您的深度学习项目。

## 下载链接

[树莓派4B安装Pytorch新版本1.3Python3.7](https://pan.quark.cn/s/ebff17fecf17)