---
layout: post
title: "PyTorch CIFAR100 实践指南"
date:   2020-08-04
tags: [100,TensorBoard,CIFAR,bash,实践]
comments: true
author: admin
---
# PyTorch CIFAR-100 实践指南

本仓库提供了一个在CIFAR-100数据集上实践多种深度学习模型的资源文件。通过本项目，您可以学习和实践以下模型：

- ResNet
- DenseNet
- VGG
- GoogleNet
- InceptionV3
- InceptionV4
- Inception-ResNetv2
- Xception
- Resnet In Resnet
- ResNext
- ShuffleNet
- ShuffleNetv2
- MobileNet
- MobileNetv2
- SqueezeNet
- NasNet
- Residual Attention Network
- SE WideResNet

## 环境要求

- Python 3.6
- PyTorch 1.6.0 + cu101
- TensorBoard 2.2.2（可选）

## 使用方法

1. **进入目录**  
   打开终端并输入以下命令：
   ```bash
   $ cd pytorch-cifar100
   ```

2. **数据集**  
   本项目将使用来自torchvision的CIFAR-100数据集，因为它更加方便。同时，我们还保留了示例代码，用于在数据集文件夹中编写您自己的数据集模块，以帮助那些不知道如何编写数据集模块的用户。

3. **运行TensorBoard（可选）**  
   如果您希望使用TensorBoard来可视化训练过程，可以按照以下步骤操作：
   - 安装TensorBoard：
     ```bash
     $ pip install tensorboard
     ```
   - 创建运行目录：
     ```bash
     $ mkdir runs
     ```
   - 运行TensorBoard：
     ```bash
     $ tensorboard --logdir=runs
     ```

## 注意事项

- 本项目旨在帮助用户在CIFAR-100数据集上实践多种深度学习模型，适合初学者和有一定经验的用户。
- 如果您有任何问题或建议，欢迎在GitHub上提交Issue或Pull Request。

希望本项目能够帮助您更好地理解和实践深度学习模型！

## 下载链接

[PyTorchCIFAR-100实践指南](https://pan.quark.cn/s/c339d5ebe10f)