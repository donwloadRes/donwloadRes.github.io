---
layout: post
title: "人脸表情识别数据集FER2013下载与处理指南"
date:   2023-07-19
tags: [path,csv,os,datasets,join]
comments: true
author: admin
---
# 人脸表情识别数据集FER2013下载与处理指南

## 简介
本资源文件提供了FER2013数据集的下载链接以及数据处理方法。FER2013数据集是一个广泛用于人脸表情识别任务的数据集，包含了多种情绪类别的图像数据。通过本指南，您可以轻松获取并处理该数据集，为后续的模型训练和实验做好准备。

## 数据集概述
FER2013数据集包含了35886张人脸表情图片，分为训练集、验证集和测试集。每张图片的大小为48x48像素，灰度图像。数据集中的表情类别包括：
- 0: 生气
- 1: 厌恶
- 2: 恐惧
- 3: 开心
- 4: 伤心
- 5: 惊讶
- 6: 中性

## 数据集下载
您可以通过提供的链接下载FER2013数据集。下载完成后，您将获得一个名为`fer2013.csv`的文件。

## 数据处理步骤
1. **分割数据集**：将`fer2013.csv`文件中的数据分割为训练集、验证集和测试集。
2. **转换为图片格式**：将分割后的数据转换为图片格式，并按照类别分别存储在不同的文件夹中。

### 代码示例
以下是数据处理的部分代码示例，帮助您将CSV文件转换为图片格式：

```python
import csv
import os
from PIL import Image
import numpy as np

datasets_path = r'path_to_datasets'
train_csv = os.path.join(datasets_path, 'train.csv')
val_csv = os.path.join(datasets_path, 'val.csv')
test_csv = os.path.join(datasets_path, 'test.csv')

train_set = os.path.join(datasets_path, 'train')
val_set = os.path.join(datasets_path, 'val')
test_set = os.path.join(datasets_path, 'test')

for save_path, csv_file in [(train_set, train_csv), (val_set, val_csv), (test_set, test_csv)]:
    if not os.path.exists(save_path):
        os.makedirs(save_path)
    num = 1
    with open(csv_file) as f:
        csvr = csv.reader(f)
        header = next(csvr)
        for i, (label, pixel) in enumerate(csvr):
            pixel = np.asarray([float(p) for p in pixel.split()]).reshape(48, 48)
            subfolder = os.path.join(save_path, label)
            if not os.path.exists(subfolder):
                os.makedirs(subfolder)
            im = Image.fromarray(pixel).convert('L')
            image_name = os.path.join(subfolder, '{:05d}.jpg'.format(i))
            im.save(image_name)
```

## 数据增强
为了提高模型的泛化能力，您可以对数据集进行数据增强操作。常见的数据增强方法包括旋转、缩放、平移、翻转等。

## 总结
通过本指南，您可以顺利下载并处理FER2013数据集，为后续的人脸表情识别任务打下坚实的基础。希望本资源对您的研究和工作有所帮助！

## 下载链接

[人脸表情识别数据集FER2013下载与处理指南](https://pan.quark.cn/s/d4458f365b84)