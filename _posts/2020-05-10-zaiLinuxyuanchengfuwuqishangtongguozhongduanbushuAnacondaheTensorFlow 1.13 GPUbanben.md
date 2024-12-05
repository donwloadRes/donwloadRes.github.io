---
layout: post
title: "在Linux远程服务器上通过终端部署Anaconda和TensorFlow 1.13 GPU版本"
date:   2020-05-06
tags: [Anaconda,TensorFlow,GPU,1.13,安装]
comments: true
author: admin
---
# 在Linux远程服务器上通过终端部署Anaconda和TensorFlow 1.13 GPU版本

欢迎阅读本指南，这里将详细指导您如何在您的Linux远程服务器上，利用终端环境高效地安装Anaconda和TensorFlow 1.13的GPU版本。此过程特别适合那些依赖强大计算能力进行深度学习开发的用户，尤其是利用如RTX 2080 Ti等高性能GPU的情况。我们将采取步骤化的方式，确保即使是初学者也能顺利完成配置。

## 目录

- 1.1 Anaconda安装
- 1.2 TensorFlow 1.13-GPU安装

### 1.1 Anaconda安装

在开始之前，确保您的远程服务器已准备好必要的网络连接和权限。Anaconda是一个强大的数据科学平台，提供了Python和R的编程环境，以及大量的预装包，非常适合数据分析和机器学习工作。

**步骤:**
1. **下载**: 首先，在本地电脑上访问Anaconda官方网站，下载对应Linux系统的Anaconda安装包，并通过Xftp上传至服务器。
2. **终端安装**: 打开Xshell，切换到上传文件的目录，使用以下命令安装：
   ```bash
   bash Anaconda3-x.x.x-Linux-x86_64.sh
   ```
   替换`x.x.x`为您实际下载的版本号，并按照提示完成安装。
3. **环境变量**: 安装后，记得将Anaconda路径添加到`.bashrc`或`.bash_profile`，以便全局访问。
   
### 1.2 TensorFlow 1.13-GPU安装

TensorFlow 1.13是广受欢迎的机器学习库之一，其GPU版本能够充分利用NVIDIA GPU加速训练。

**前置条件**:
- 确认NVIDIA驱动已正确安装并验证通过`nvidia-smi`命令。
- 安装CUDA工具包和cuDNN库，具体版本需与TensorFlow兼容。对于TensorFlow 1.13，建议使用CUDA 10.0和对应的cuDNN版本。

**安装步骤:**
1. **创建虚拟环境**: 使用Anaconda创建一个新的Python环境以隔离TensorFlow安装。
   ```bash
   conda create -n tf_gpu python=3.6
   conda activate tf_gpu
   ```
2. **安装TensorFlow GPU版**:
   ```bash
   conda install tensorflow-gpu=1.13
   ```

至此，您应该已经成功地在远程Linux服务器上搭建好了支持GPU的TensorFlow 1.13环境，可以开始您的数据科学之旅了！

**版权说明**：
本文档基于共享知识的原则编写，旨在帮助读者有效设置开发环境。请尊重原创内容，遵守CC 4.0 BY-SA版权协议。任何形式的分享或引用都应包含本指南的原作者信息。

## 下载链接

[在Linux远程服务器上通过终端部署Anaconda和TensorFlow1.13GPU版本分享](https://pan.quark.cn/s/20c525b1cf6c)