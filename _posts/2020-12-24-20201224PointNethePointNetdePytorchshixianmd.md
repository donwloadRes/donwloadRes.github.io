---
layout: post
title: "PointNet和PointNet++的Pytorch实现"
date:   2020-01-31
tags: [--,PointNet,分割,代码,模型]
comments: true
author: admin
---
# PointNet和PointNet++的Pytorch实现

## 资源描述

本仓库提供了PointNet和PointNet++的Pytorch实现，适用于点云数据的分类、分割和语义分割任务。以下是资源的主要更新和功能介绍：

### 更新日志

- **2021/03/27**
  - 发布语义分割的预训练模型，其中PointNet++可以达到53.5%的mIoU。
  - 发布预训练模型用于分类和部分分割，存放在`log/`目录下。

- **2021/03/20**
  - 更新分类代码，包括：
    1. 添加训练ModelNet10数据集的代码，使用`--num_category 10`。
    2. 添加仅在CPU上运行的代码，使用`--use_cpu`。
    3. 增加离线数据预处理代码，加速训练，使用`--process_data`。
    4. 添加用于均匀采样训练的代码，使用`--use_uniform_sample`。

- **2019/11/26**
  - 修复了之前代码中的一些错误并增加了数据增强技巧。现在只用1024个点就可以达到92.8%的分类准确率！
  - 增加了测试代码，包括分类和分割，以及可视化的语义分割。
  - 将所有模型整理成`./models`文件夹，方便使用。

## 使用说明

1. **分类任务**：
   - 使用`--num_category`参数指定数据集类别数。
   - 使用`--use_cpu`参数在CPU上运行代码。
   - 使用`--process_data`参数进行离线数据预处理。
   - 使用`--use_uniform_sample`参数进行均匀采样训练。

2. **分割任务**：
   - 使用预训练模型进行语义分割，模型存放在`log/`目录下。
   - 使用测试代码进行分类和分割任务，并进行可视化。

3. **数据增强**：
   - 代码中已包含数据增强技巧，可以进一步提升模型性能。

## 模型文件

所有模型文件已整理至`./models`文件夹，方便用户直接调用和使用。

## 注意事项

- 请确保在使用前安装所需的Pytorch版本和相关依赖库。
- 对于不同的任务，请根据需要调整参数和模型配置。

希望本仓库的实现能够帮助您在点云数据处理任务中取得更好的效果！

## 下载链接

[PointNet和PointNet的Pytorch实现](https://pan.quark.cn/s/6a55074f31ef)