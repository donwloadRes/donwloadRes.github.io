---
layout: post
title: "小白第一次跑YOLOv3模型经历"
date:   2021-11-14
tags: [YOLOv3,训练,文件夹,PyTorch,下载]
comments: true
author: admin
---
# 小白第一次跑YOLOv3模型经历

本文详细记录了在Windows 11系统下使用PyCharm和PyTorch搭建YOLOv3环境的全过程，包括模型下载、数据集准备、训练文件创建、预训练权重加载以及如何运行Train.py和Detect.py进行目标检测。

## 环境搭建

### 1. 系统与工具
- **操作系统**: Windows 11
- **编程工具**: PyCharm
- **Python版本**: 3.11
- **GPU**: CUDA 11.8
- **框架**: PyTorch

### 2. 模型代码下载
- 模型代码下载地址：[YOLOv3 GitHub仓库](https://github.com/ultralytics/yolov3)
- 本文使用的是9.5.0版本，需要在GitHub仓库中选择历史版本进行下载。

### 3. 数据集准备
- 本文使用的是VOCdevkit数据集，包含Annotationa文件和JPEGimages文件，分别包含9964个xml文件和对应的9964个jpg文件。

### 4. 创建训练文件
- 在VOCdevkit文件夹下新建images和labels文件夹，分别用于存放训练和测试数据。
- 在images和labels文件夹下分别新建train和val文件夹。

### 5. 预训练权重加载
- 加载预训练权重可以缩短训练时间并提高精度。
- 预训练权重下载地址：[YOLOv3权重下载](https://github.com/ultralytics/yolov3/releases)

## 运行环境搭建

### 1. PyTorch框架
- 安装PyTorch及其依赖包，使用清华镜像源加速下载。

### 2. CUDA和cuDNN安装
- 安装CUDA和cuDNN，确保显卡驱动和CUDA版本匹配。

### 3. 验证GPU环境
- 在PyCharm的Terminal中输入命令验证PyTorch是否支持GPU运行。

## 模型训练与检测

### 1. 运行Train.py
- 设置训练参数，如batch size和epoch数，根据设备算力进行适当调整。
- 训练结果保存在runs/train/exp/weights文件夹下。

### 2. 运行Detect.py
- 使用自定义图片、视频或摄像头进行目标检测。

## 总结

本文详细介绍了在Windows 11系统下搭建YOLOv3环境的全过程，适合初学者参考。通过本文的指导，小白也能顺利运行YOLOv3模型并进行目标检测。

## 下载链接

[小白第一次跑YOLOv3模型经历](https://pan.quark.cn/s/f46820780127)