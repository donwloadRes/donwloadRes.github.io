---
layout: post
title: "Windows 10 复现 DEtection TRansformers（DETR）并实现自己的数据集"
date:   2023-09-11
tags: [DETR,训练,模型,Windows,10]
comments: true
author: admin
---
# Windows 10 复现 DEtection TRansformers（DETR）并实现自己的数据集

本资源文件旨在帮助用户在Windows 10系统上复现DEtection TRansformers（DETR）模型，并实现自己的数据集训练。DETR是Facebook AI研究者提出的Transformer视觉版本，用于目标检测和全景分割，是第一个将Transformer成功整合为目标检测框架中心构建块的模型。

## 内容概述

1. **代码地址**：提供了DETR模型的Github代码地址。
2. **论文地址**：提供了相关论文的地址。
3. **环境配置**：详细介绍了如何在Windows 10系统上配置环境，包括安装必要的库和解决常见问题。
4. **数据集准备**：指导用户如何准备自己的训练集，包括数据标记、文件组织和格式转换。
5. **模型训练**：提供了详细的训练步骤和参数设置。
6. **模型测试**：介绍了如何使用训练好的模型进行测试，并提供了测试代码的修改方法。

## 使用步骤

### 第一步：环境配置

1. 下载代码并使用PyCharm打开。
2. 运行终端，输入 `pip install -r requirements.txt` 安装必要的库。
3. 解决安装过程中可能遇到的问题，如cocoapi安装失败等。

### 第二步：数据集准备

1. 使用自己的数据标记工具（如labelimg）创建VOC类型的数据集。
2. 将标记好的数据文件组织到指定文件夹中。
3. 将VOC格式的数据转换为json格式。

### 第三步：模型训练

1. 修改DETR代码中的num_classes参数，以匹配自己的数据集类别数。
2. 运行训练脚本进行模型训练。

### 第四步：模型测试

1. 修改测试代码中的图片路径和类别名称。
2. 使用训练好的模型进行测试，并查看结果。

## 常见问题

- 在安装cocoapi时遇到问题，可以尝试本地安装或使用其他大神编译好的包。
- 遇到vc++2015等问题，建议在VS Studio中安装C++相关组件。

## 注意事项

- 确保所有路径和文件名正确无误。
- 根据实际情况调整训练参数，如epochs、batch_size等。

通过本资源文件，用户可以在Windows 10系统上顺利复现DETR模型，并使用自己的数据集进行训练和测试。

## 下载链接

[Windows10复现DEtectionTRansformersDETR并实现自己的数据集](https://pan.quark.cn/s/66b47a6f1abb)