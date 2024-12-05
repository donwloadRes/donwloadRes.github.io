---
layout: post
title: "CUDA11.4、CUDNN、Pytorch安装指南"
date:   2022-04-04
tags: [CUDA,安装,Pytorch,cuDNN,版本]
comments: true
author: admin
---
# CUDA11.4、CUDNN、Pytorch安装指南

本仓库提供了一个详细的安装指南，帮助用户在系统中安装CUDA 11.4、CUDNN以及Pytorch。以下是安装步骤的简要概述：

## 1. 显卡驱动查看
首先，确保您的系统已安装适当的NVIDIA显卡驱动。可以通过NVIDIA控制面板查看显卡驱动版本。

## 2. 安装CUDA
### 下载CUDA
您可以通过以下两种方法下载CUDA：
- **方法一**：访问CUDA Toolkit官网下载最新版本的CUDA。
- **方法二**：通过百度搜索特定版本的CUDA Toolkit（如11.4或10.0）进行下载。

### CUDA环境配置
安装完成后，配置系统环境变量，将CUDA的安装路径添加到系统路径中。

### 验证CUDA安装
打开命令窗口，输入`nvcc -V`，确认CUDA是否安装成功。

## 3. 安装cuDNN
### 下载cuDNN
访问cuDNN官网，下载与CUDA版本对应的cuDNN库。

### cuDNN安装步骤
将下载的cuDNN压缩文件解压，并将解压后的文件夹复制到CUDA的安装目录中。

### 验证cuDNN安装
通过执行`deviceQuery.exe`和`bandwidthTest.exe`，确认cuDNN是否安装成功。

## 4. 安装Pytorch
### 创建虚拟环境
使用conda创建一个新的虚拟环境，并激活该环境。

### 安装Pytorch
在激活的虚拟环境中，使用conda命令安装Pytorch及其相关组件。

### 验证Pytorch安装
在Python环境中导入torch库，确认Pytorch是否安装成功。

## 注意事项
- 确保CUDA和cuDNN的版本匹配。
- 在安装Pytorch时，注意选择与CUDA版本兼容的Pytorch版本。

通过以上步骤，您应该能够成功在系统中安装并配置CUDA 11.4、CUDNN以及Pytorch。如果在安装过程中遇到任何问题，请参考相关文档或社区支持。

## 下载链接

[CUDA11.4CUDNNPytorch安装指南](https://pan.quark.cn/s/798640450929)