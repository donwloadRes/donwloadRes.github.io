---
layout: post
title: "Pytorch环境详细安装教程Win10CUDA升级116cudNNAnaconda3虚拟环境pycharm"
date:   2023-10-12
tags: [CUDA,11.6,虚拟环境,PyTorch,安装]
comments: true
author: admin
---
# Pytorch环境详细安装教程【Win10+CUDA升级11.6+cudNN+Anaconda3虚拟环境+pycharm】

欢迎来到PyTorch环境配置指南，本教程专为Windows 10用户设计，旨在帮助您从零开始，一步步搭建高效的深度学习开发环境。无论你是初学者还是已经有一定经验的开发者，通过本文档，你将能够顺利完成PyTorch及其相关依赖的安装，包括最新的CUDA 11.6和cudNN的适配，以及如何在Anaconda3虚拟环境中进行操作，最后集成到PyCharm这一强大的IDE中，让你的深度学习之旅更加顺畅。

## 前提条件

- **操作系统**: Windows 10 64位
- **硬件需求**: NVIDIA GPU（支持CUDA）
- **Python版本**: 推荐Python 3.7或更高版本
- **工具软件**: Anaconda3、PyCharm Community/Professional Edition

## 安装步骤

### 1. 安装Anaconda3

首先，访问Anaconda官网下载最新版Anaconda3，并按照官方指引完成安装。记得在安装过程中勾选“添加到PATH环境变量”选项。

### 2. 创建虚拟环境

打开Anaconda Prompt，创建一个名为pytorch_env的新虚拟环境，指定Python版本：
```
conda create -n pytorch_env python=3.7
```
激活虚拟环境：
```
conda activate pytorch_env
```

### 3. 安装PyTorch与CuDNN

根据你的系统配置（CPU/GPU, CUDA版本），访问PyTorch官方网站的安装指令页获取适合的命令。对于CUDA 11.6，执行如下命令（以GPU为例）：
```
conda install pytorch torchvision torchaudio cudatoolkit=11.6 -c pytorch
```

### 4. 升级CUDA（如果已安装旧版本）

确保遵循 NVIDIA 的官方指南来安全升级CUDA至11.6。卸载旧版本后，从官方网站下载并安装CUDA 11.6工具包。

### 5. 安装cudNN

前往NVIDIA官网下载对应CUDA 11.6版本的cudNN库，解压并将库文件复制到CUDA的相应目录下。

### 6. 集成PyCharm

- 在PyCharm中，创建一个新的项目，选择之前创建的虚拟环境作为解释器。
- 确保所有必要的库已经在虚拟环境中安装。

## 测试环境

安装完成后，可以通过运行以下简单的代码片段来测试PyTorch是否正确安装：
```python
import torch
print(torch.__version__)
device = torch.device('cuda' if torch.cuda.is_available() else 'cpu')
print(f'Using {device} device')
```

若一切顺利，你应该能看到PyTorch的版本号，并确认GPU是否可用。

以上便是完整的PyTorch环境配置流程。遇到具体问题时，详细的解决办法可参考原始文章在CSDN上的详细说明。祝您配置成功，编程愉快！

## 下载链接

[Pytorch环境详细安装教程Win10CUDA升级11.6cudNNAnaconda3虚拟环境pycharm](https://pan.quark.cn/s/1cee5f054356)