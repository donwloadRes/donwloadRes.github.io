---
layout: post
title: "INRIA数据集介绍"
date:   2024-11-02
tags: [样本,大小不一,训练,images,pos]
comments: true
author: admin
---
# INRIA数据集介绍

## 概述
INRIA数据集是一个广泛用于行人检测研究的数据集。该数据集包含了大量室外场景中的行人图像，涵盖了不同的光照条件、行人姿态和背景复杂度，非常适合用于评估和训练行人检测算法。

## 数据集内容
INRIA数据集主要包含以下内容：
- **原始图像**：来自GRAZ 01数据集和网络上的图片，每张图片中都进行了行人区域的标定。
- **归一化图像**：原始图像经过归一化处理后的版本，通常用于重现实验。
- **标注信息**：包括行人区域的矩形框坐标和尺寸信息。

## 数据集结构
数据集的目录结构如下：
- **INRIADATA**
  - **normalized_images**
    - **train**
      - **pos**：96x160大小的训练正样本，需要裁剪中间的64x128大小。
      - **neg**：大小不一的训练负样本，通常是几百乘几百，需要从每张图中随机裁剪10个区域作为训练负样本。
    - **test**
      - **pos**：大小不一的测试正样本。
      - **neg**：大小不一的测试负样本。
  - **original_images**
    - **train**
      - **pos**：大小不一的训练正样本。
      - **neg**：大小不一的训练负样本。
      - **annotations**：标注信息。
    - **test**
      - **pos**：大小不一的测试正样本。
      - **neg**：大小不一的测试负样本。
      - **annotations**：标注信息。

## 使用方法
1. **训练**：可以选择使用`normalized_images`目录下的图片进行训练，或者使用`original_images`目录下的图片和标注信息进行训练。
2. **测试**：在`original_images/test/pos`目录下进行测试。

## 注意事项
- 数据集中的部分目录使用了软链接，建议在Linux系统下解压和使用。
- 部分图像的命名和标注信息可能存在不一致或错误，使用时需注意。

## 参考文献
该数据集主要用于行人检测研究，参考文献包括：
- Navneet Dalal的博士毕业论文。
- Histograms of Oriented Gradients for Human Detection。

## 贡献
欢迎对该数据集的使用和改进提出建议和贡献。

## 下载链接

[INRIA数据集介绍分享](https://pan.quark.cn/s/523b6fdb9655)