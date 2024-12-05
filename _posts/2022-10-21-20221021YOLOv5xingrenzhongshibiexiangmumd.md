---
layout: post
title: "YOLOv5行人重识别项目"
date:   2024-07-11
tags: [训练,视频,人员,行人,检测]
comments: true
author: admin
---
# YOLOv5行人重识别项目

## 项目简介

本项目结合了YOLOv5目标检测模型和行人重识别（ReID）技术，旨在实现跨视频的行人检测与重识别功能。通过本项目，用户可以训练自己的行人重识别模型，并在视频中进行行人检测和跨视频的人员追踪。

## 主要功能

1. **行人重识别训练**：支持多种主干网络（如resnet50, resnet50_ibn_a, se_resnext50等），用户可以根据需求选择合适的网络进行训练。
2. **继续训练与微调**：支持中断后的继续训练或微调训练，方便用户在已有模型的基础上进行进一步优化。
3. **冻结训练**：提供冻结训练功能，加快网络前期训练速度。
4. **TensorBoard可视化**：支持训练过程中的评价指标、困难样本可视化，方便用户监控训练进度和效果。
5. **人员标注**：支持视频中的人员标注功能，用户可以通过鼠标框选标注特定人员。
6. **跨视频人员检测**：支持跨视频的人员检测功能，可以在不同摄像头拍摄的视频中追踪同一人员。

## 环境要求

- matplotlib>=3.2.2
- numpy>=1.18.5
- opencv-python>=4.1.2
- Pillow>=7.1.2
- PyYAML>=5.3.1
- requests>=2.23.0
- scipy>=1.4.1
- torch>=1.7.0
- torchvision>=0.8.1
- tqdm>=4.41.0
- pytorch-ignite=0.4.11

## 使用说明

### 训练模型

1. 下载代码并配置环境。
2. 准备训练数据集，并进行数据预处理。
3. 运行训练脚本，开始模型训练。

### 测试模型

1. 使用训练好的模型进行测试，获取测试结果（如mAP、Rank等指标）。
2. 可以通过TensorBoard查看训练过程中的评价指标和困难样本。

### 人员标注与查找

1. 使用人员标注工具对视频中的特定人员进行标注。
2. 运行人员查找脚本，实现跨视频的人员检测和追踪。

## 注意事项

- 本项目部分功能有偿提供，具体详情请联系项目开发者。
- 训练和检测是两个独立的项目，使用时需分别配置。

## 联系我们

如有任何问题或建议，请联系项目开发者。

## 下载链接

[YOLOv5行人重识别项目](https://pan.quark.cn/s/5686af63d220)