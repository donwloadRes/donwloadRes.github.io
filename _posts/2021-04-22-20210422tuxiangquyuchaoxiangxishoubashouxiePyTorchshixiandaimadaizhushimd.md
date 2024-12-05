---
layout: post
title: "图像去雨：超详细手把手写 PyTorch 实现代码（带注释）"
date:   2024-05-03
tags: [图像,训练,代码,PyTorch,模型]
comments: true
author: admin
---
# 图像去雨：超详细手把手写 PyTorch 实现代码（带注释）

## 项目介绍

本项目提供了一个使用 PyTorch 实现的图像去雨代码，代码中包含了详细的注释，适合初学者学习和实践。通过本项目，您可以了解如何使用深度学习方法去除图像中的雨水，包括数据集准备、训练数据集和测试数据集的代码实现、网络模型定义、训练过程以及测试过程。

## 主要内容

1. **数据集准备**：
   - 使用公开的 Rain12600 和 Rain1400 数据集。
   - 训练图像 900 张，测试图像 100 张，分别有 14 张不同的雨图。
   - 训练集共 12600 对，测试集共 1400 对。

2. **训练数据集代码**：
   - 使用 PyTorch 的 Dataset 类自定义训练数据集。
   - 对输入图像和标签图像进行预处理，包括中心裁剪和转换为张量。

3. **测试数据集代码**：
   - 使用 PyTorch 的 Dataset 类自定义测试数据集。
   - 对输入图像进行预处理，转换为张量。

4. **网络模型代码**：
   - 基于 PRN 网络模型进行定义。
   - 包含多个卷积层和残差块，用于提取图像特征并去除雨水。

5. **训练代码**：
   - 使用 Adam 优化器和 MSELoss 损失函数进行训练。
   - 支持从已有的模型继续训练或从头开始训练。

6. **测试代码**：
   - 加载训练好的模型参数，对测试集图像进行去雨处理。
   - 将处理后的图像保存为 JPG 格式。

## 使用方法

1. **数据集下载**：
   - 下载 Rain12600 和 Rain1400 数据集，并按照代码中的路径进行存放。

2. **训练模型**：
   - 运行 `Train.py` 文件，开始训练模型。
   - 训练过程中会保存模型参数，方便后续使用。

3. **测试模型**：
   - 运行 `Test.py` 文件，加载训练好的模型对测试集图像进行去雨处理。
   - 处理后的图像会自动保存到指定路径。

## 依赖库

- PyTorch
- torchvision
- PIL
- matplotlib

## 参考文献

- Xueyang Fu, Jiabin Huang, Delu Zeng, et al. Removing Rain From Single Images via a Deep Detail Network[C]. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition, 2017:3855-3863.
- Dongwei Ren, Wangmeng Zuo, Qinghua Hu, et al. Progressive Image Deraining Networks: A Better and Simpler Baseline[C]. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition, 2019:3937-3946.

## 其他说明

- 本项目代码仅供参考，具体实现细节可根据需求进行调整。
- 数据集的制作和预处理部分可根据实际情况进行修改。

## 作者

- 听 风、

## 版权声明

- 本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[图像去雨超详细手把手写PyTorch实现代码带注释分享](https://pan.quark.cn/s/4179db9d4c6f)