---
layout: post
title: "Windows Python PyTorch CUDA 11.7 TensorRT 环境配置指南"
date:   2023-08-17
tags: [CUDA,TensorRT,py,detect,PyTorch]
comments: true
author: admin
---
# Windows Python PyTorch CUDA 11.7 TensorRT 环境配置指南

本仓库提供了一个详细的指南，帮助你在Windows系统上配置Python、PyTorch、CUDA 11.7和TensorRT环境。通过本指南，你可以轻松搭建一个支持GPU加速的深度学习开发环境。

## 内容概述

1. **版本说明**
   - 详细介绍了所使用的工具版本，包括Nvidia驱动、CUDA、TensorRT、cuDNN和PyTorch。

2. **版本选择**
   - 提供了如何选择合适的Python和CUDA版本的建议。

3. **下载代码**
   - 指导如何下载和克隆代码到本地路径。

4. **创建并激活虚拟环境**
   - 使用Conda创建并管理Python虚拟环境。

5. **使用CPU推理**
   - 安装工程运行的最少依赖，并运行detect.py进行CPU推理。

6. **使用Nvidia GPU推理**
   - 配置CUDA环境，安装PyTorch CUDA版本，并运行detect.py进行GPU推理。

7. **安装TensorRT**
   - 提供了安装TensorRT的步骤，并指导如何导出engine文件。

8. **额外配置**
   - 提供了一些额外的配置步骤，确保TensorRT环境正常运行。

## 使用步骤

1. **下载代码**
   - 将代码下载或克隆到本地路径，例如`C:\mrathena\develop\workspace\pycharm\yolo v5 7.0`。

2. **创建并激活虚拟环境**
   - 使用Conda创建虚拟环境：
     ```bash
     conda create -n yolo python=3.10
     conda activate yolo
     ```

3. **使用CPU推理**
   - 安装工程运行的最少依赖：
     ```bash
     cd C:\mrathena\develop\workspace\pycharm\yolo v5 7.0
     pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple
     ```
   - 运行detect.py进行CPU推理。

4. **使用Nvidia GPU推理**
   - 安装PyTorch CUDA环境：
     ```bash
     pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117
     ```
   - 运行detect.py进行GPU推理。

5. **安装TensorRT**
   - 安装TensorRT模块：
     ```bash
     pip install tensorrt-8.5.2.2-cp310-none-win_amd64.whl
     ```
   - 安装ONNX：
     ```bash
     pip install onnx -i https://pypi.tuna.tsinghua.edu.cn/simple
     ```
   - 导出engine文件：
     ```bash
     python export.py --weights yolov5s.pt --device 0 --include engine
     ```

6. **运行detect.py**
   - 修改detect.py中的weights参数为engine文件，然后运行detect.py。

## 注意事项

- 确保你的Nvidia驱动程序支持CUDA 11.7。
- 如果遇到`NotImplementedError: Could not run 'torchvision::nms' with arguments from the 'CUDA' backend`错误，请检查并替换为正确的torchvision版本。
- 确保所有依赖库版本兼容，避免版本冲突。

通过本指南，你可以顺利配置Windows上的Python、PyTorch、CUDA 11.7和TensorRT环境，为深度学习开发提供强大的GPU支持。

## 下载链接

[WindowsPythonPyTorchCUDA11.7TensorRT环境配置指南](https://pan.quark.cn/s/658b1f818558)