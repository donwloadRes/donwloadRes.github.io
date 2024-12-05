---
layout: post
title: "深度学习环境配置指南：Windows下TensorFlow-GPU 2.4.0配置"
date:   2020-06-23
tags: [安装,TensorFlow,GPU,Anaconda,Windows]
comments: true
author: admin
---
# 深度学习环境配置指南：Windows下TensorFlow-GPU 2.4.0配置

## 简介
本资源文件提供了在Windows操作系统下，使用30系显卡配置TensorFlow-GPU 2.4.0环境的详细步骤。通过本指南，您可以顺利搭建一个支持GPU加速的深度学习开发环境。

## 环境要求
- 操作系统：Windows
- 显卡：30系显卡（或其他支持CUDA 11.0的显卡）
- Python版本：3.7

## 配置步骤

### 1. Anaconda安装
1. **下载Anaconda**：
   - 可以选择下载新版或旧版的Anaconda。
   - 旧版Anaconda包含VSCode，方便后续安装。

2. **安装Anaconda**：
   - 选择安装位置，建议不安装在C盘。
   - 勾选“Add Anaconda to my PATH environment variable”以自动添加到系统环境变量。

### 2. Cudnn和CUDA的下载和安装
1. **下载Cudnn和CUDA**：
   - 下载与TensorFlow-GPU 2.4.0兼容的CUDA 11.0和Cudnn 8.0.5.39。

2. **安装Cudnn和CUDA**：
   - 运行下载的exe文件进行安装。
   - 将Cudnn的内容解压并复制到CUDA的安装目录下。

### 3. 配置TensorFlow-GPU环境
1. **创建并激活环境**：
   - 使用命令`conda create –n tensorflow2-gpu python=3.7`创建环境。
   - 使用命令`activate tensorflow2-gpu`激活环境。

2. **安装TensorFlow-GPU**：
   - 在激活的环境中，使用命令`pip install tensorflow-gpu==2.4.0`安装TensorFlow-GPU。

3. **安装其他依赖库**：
   - 安装必要的依赖库，如`scipy`, `numpy`, `matplotlib`, `opencv-python`, `tqdm`, `Pillow`, `h5py`等。

### 4. 安装VSCode
1. **下载并安装VSCode**：
   - 从官网下载VSCode并进行安装。
   - 安装时勾选“Add 'Open with Code' action to Windows Explorer file context menu”以方便右键打开文件夹。

2. **在Anaconda中安装VSCode**：
   - 打开Anaconda，切换到TensorFlow-GPU环境。
   - 安装VSCode并固定到任务栏，方便后续使用。

## 注意事项
- 如果在安装过程中遇到`SubProcess ended with return code: 4294967295`错误，可以尝试将CUDA版本从11.0改为11.2。
- 安装过程中如果下载较慢，建议更换pip源。

## 总结
通过以上步骤，您可以在Windows系统下成功配置TensorFlow-GPU 2.4.0环境，并利用30系显卡进行高效的深度学习开发。

## 下载链接

[深度学习环境配置指南Windows下TensorFlow-GPU2.4.0配置分享](https://pan.quark.cn/s/1638e48164ef)