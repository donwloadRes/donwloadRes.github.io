---
layout: post
title: "PyTorch图像分类完整代码实现"
date:   2024-03-31
tags: [模型,PyTorch,TTA,部署,使用]
comments: true
author: admin
---
# PyTorch图像分类完整代码实现

本仓库提供了一个利用PyTorch实现图像分类的完整代码，涵盖了从训练、预测、测试时增强（TTA）、模型融合、模型部署、CNN特征提取到使用SVM、随机森林等分类器的全流程。代码实现了多种功能，包括带有warmup的cosine学习率调整、多模型融合预测、使用Flask + Redis实现模型云端API部署、C++ LibTorch的模型部署、TTA测试时增强、标签平滑、CNN特征提取与分类器结合等。

## 功能列表

1. **基础功能**：
   - 利用PyTorch实现图像分类。
   - 带有warmup的cosine学习率调整。
   - 多模型融合预测，包括加权与投票融合。

2. **模型部署**：
   - 使用Flask + Redis实现模型云端API部署（tag v1）。
   - C++ LibTorch的模型部署。

3. **测试时增强（TTA）**：
   - 使用TTA进行预测（tag v1）。

4. **标签平滑**：
   - 添加标签平滑的PyTorch实现（tag v1）。

5. **特征提取与分类**：
   - 使用CNN提取特征，并使用SVM、随机森林（RF）、多层感知机（MLP）、KNN等分类器进行分类（tag v1）。
   - 可视化特征层。

## 使用说明

1. **训练模型**：
   - 使用提供的训练脚本进行模型训练，支持多种学习率调整策略。

2. **模型预测**：
   - 使用预测脚本进行单张图片或批量图片的预测。

3. **模型融合**：
   - 支持多模型融合预测，可以通过加权或投票方式进行融合。

4. **模型部署**：
   - 使用Flask + Redis实现模型云端API部署，方便远程调用。
   - 使用C++ LibTorch进行模型部署，适用于高性能需求场景。

5. **TTA测试时增强**：
   - 使用TTA进行预测，提高模型预测的鲁棒性。

6. **标签平滑**：
   - 在训练过程中使用标签平滑，减少模型过拟合。

7. **特征提取与分类**：
   - 使用CNN提取图像特征，并结合SVM、随机森林等分类器进行分类。
   - 可视化特征层，便于分析模型中间层的表现。

## 注意事项

- 本代码基于PyTorch实现，建议使用PyTorch 1.x版本。
- 模型部署部分需要安装Flask、Redis等依赖库。
- 特征提取与分类部分需要安装scikit-learn等库。

## 参考

本代码参考了[lxztju/pytorch_classification](https://github.com/lxztju/pytorch_classification)项目，感谢原作者的贡献。

## 下载链接

[PyTorch图像分类完整代码实现](https://pan.quark.cn/s/59883e18d8df)