---
layout: post
title: "win11+RTX4070Ti 安装 CUDA + cuDNN 图文教程"
date:   2020-09-26
tags: [CUDA,安装,cuDNN,教程,显卡]
comments: true
author: admin
---
# win11+RTX4070Ti 安装 CUDA + cuDNN 图文教程

本资源文件提供了一个详细的图文教程，指导如何在Windows 11系统上安装CUDA和cuDNN，适用于配备RTX 4070Ti显卡的电脑。教程包括检查显卡驱动更新、下载安装CUDA、验证安装及cuDNN的安装和验证过程。

## 教程内容概述

1. **查看电脑是否有最新显卡驱动并确定已安装**
   - 使用GeForce Experience自动检查更新。
   - 确认显卡驱动支持的最高CUDA版本。

2. **下载CUDA**
   - 从NVIDIA官网下载最新版本的CUDA。
   - 注意选择与TensorFlow或PyTorch兼容的CUDA版本。

3. **安装CUDA**
   - 双击运行安装程序，选择自定义安装并完成安装。
   - 配置环境变量，确保CUDA安装成功。

4. **安装cuDNN**
   - 下载与CUDA版本对应的cuDNN。
   - 解压文件并将bin、include、lib文件夹复制到CUDA安装目录。

5. **验证cuDNN是否安装成功**
   - 执行bandwidthTest.exe和deviceQuery.exe，确认安装成功。

## 注意事项

- 本教程为2023年12月4日更新，适用于Windows 11家庭版操作系统。
- 教程中使用的电脑配置为i7-13700KF+RTX4070Ti。
- 安装过程中请确保网络连接稳定，以便顺利下载所需文件。

## 资源文件内容

- 教程详细步骤的图文说明。
- 必要的安装文件（已下载并提供网盘链接）。

通过本教程，您将能够顺利在Windows 11系统上安装CUDA和cuDNN，为深度学习和并行计算提供强大的GPU支持。

## 下载链接

[win11RTX4070Ti安装CUDAcuDNN图文教程](https://pan.quark.cn/s/086df9a6bebd)