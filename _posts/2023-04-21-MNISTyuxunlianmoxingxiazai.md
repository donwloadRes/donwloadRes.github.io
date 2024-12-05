---
layout: post
title: "MNIST预训练模型下载"
date:   2021-08-18
tags: [MNIST,模型,FGSM,pth,训练]
comments: true
author: admin
---
# MNIST预训练模型下载

## 资源文件介绍

本仓库提供了一个名为 `MNIST预训练模型.pth` 的资源文件，该文件是用于在 FGSM（Fast Gradient Sign Method）中对 MNIST 数据集进行白盒测试的预训练模型。

## 文件用途

`MNIST预训练模型.pth` 文件包含了在 MNIST 数据集上训练好的模型权重，可以直接用于 FGSM 攻击实验中的白盒测试。通过加载该模型，用户可以快速进行对抗样本生成和攻击效果评估。

## 使用方法

1. **下载文件**：点击仓库中的 `MNIST预训练模型.pth` 文件进行下载。
2. **加载模型**：在您的代码中使用 PyTorch 或其他支持 `.pth` 文件的框架加载该模型。
3. **进行测试**：使用加载的模型进行 FGSM 攻击实验，评估模型的鲁棒性。

## 注意事项

- 该模型仅适用于 MNIST 数据集的白盒测试，不适用于其他数据集或任务。
- 在使用该模型进行 FGSM 攻击时，请确保您已经理解了 FGSM 的基本原理和实现方法。

## 联系我们

如果您在使用过程中遇到任何问题或有任何建议，欢迎通过仓库的 Issues 功能联系我们。

## 下载链接

[MNIST预训练模型下载](https://pan.quark.cn/s/beb84d83847a)