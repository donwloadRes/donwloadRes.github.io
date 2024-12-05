---
layout: post
title: "WindowsAnaconda安装AlphaPose2023829"
date:   2022-12-27
tags: [AlphaPose,bash,install,安装,conda]
comments: true
author: admin
---
# Windows+Anaconda安装AlphaPose（2023.8.29）

## 简介

本资源文件提供了在Windows操作系统上使用Anaconda安装AlphaPose的详细步骤和解决方案。AlphaPose是一个开源的姿态估计工具，广泛应用于计算机视觉领域。通过本指南，您可以轻松地在Windows环境下配置和运行AlphaPose。

## 安装步骤

### 第一步：创建虚拟环境

首先，使用Anaconda创建一个新的虚拟环境：

```bash
conda create -n alphapose python=3.7 -y
conda activate alphapose
```

### 第二步：安装PyTorch

根据官方文档的命令安装PyTorch：

```bash
conda install pytorch torchvision torchaudio pytorch-cuda=11.3 -c pytorch -c nvidia
```

如果遇到版本不匹配的问题，可以参考PyTorch官网提供的命令进行安装：

```bash
conda install pytorch==1.12.1 torchvision==0.13.1 torchaudio==0.12.1 cudatoolkit=11.3 -c pytorch
```

### 第三步：下载AlphaPose

从GitHub克隆AlphaPose仓库并进入对应文件夹：

```bash
git clone https://github.com/MVIG-SJTU/AlphaPose.git
cd AlphaPose
```

### 第四步：安装依赖包

根据官方文档，首先将CUDA路径添加到系统环境变量中：

```bash
set PATH=C:\path\to\cuda\bin
set LD_LIBRARY_PATH=C:\path\to\cuda\lib64
```

然后安装其他必要的包：

```bash
python -m pip install cython
pip install numpy
conda install matplotlib
conda install scipy
```

### 第五步：安装AlphaPose

运行以下命令安装AlphaPose：

```bash
python setup.py build develop
```

如果遇到错误，可以尝试额外安装`cython-bbox`模块：

```bash
python -m pip install git+https://github.com/yanfengliu/cython_bbox.git
```

### 第六步：下载模型

手动下载对象检测模型`yolov3-spp.weights`，并将其放入`/detector/yolo/data`目录中。如果使用YOLOX作为检测器，可以下载相应的权重并放入`/detector/yolox/data`目录中。

### 第七步：运行模型

以Multi Domain Models中的Fast Pose为例，在命令行中执行以下命令：

```bash
python scripts/demo_inference.py --cfg configs/halpe_coco_wholebody_136/resnet/256x192_res50_lr1e-3_2x-regression.yaml --checkpoint pretrained_models/multi_domain_fast50_regression_256x192.pth --indir examples/demo/ --save_img --gpus -1
```

## 常见问题

- **CUDA版本不匹配**：确保安装的CUDA版本与PyTorch兼容。
- **内存不足**：如果遇到CUDA内存不足的问题，可以尝试在服务器上运行或使用CPU版本。

## 总结

通过以上步骤，您可以在Windows环境下成功安装并运行AlphaPose。如果在安装过程中遇到任何问题，请参考相关文档或社区讨论。

## 下载链接

[WindowsAnaconda安装AlphaPose2023.8.29分享](https://pan.quark.cn/s/c43193d4334e)