---
layout: post
title: "ResNetAttention ResNet  注意力机制"
date:   2024-08-08
tags: [--,ResNet,epoch,CIFAR10,device]
comments: true
author: admin
---
# ResNet_Attention: ResNet + 注意力机制

## 资源描述

本仓库提供了一个名为 `ResNet_Attention` 的资源文件，该文件结合了 ResNet 和注意力机制（包括 CBAM 和 SE）。该模型主要用于图像分类任务，特别是在 CIFAR10 数据集上的训练和验证。

## 环境要求

- 操作系统：Ubuntu 20.04
- GPU：GTX 1080Ti
- Python 版本：3.7
- PyTorch 版本：1.7.0
- CUDA 版本：10.2
- CuDNN 版本：7.0

## 使用方法

### 训练模型

#### 使用 SE 注意力机制训练

```bash
python train_CIFAR10.py --prefix 4 --device 1 --epoch 160 --att_type se
```

#### 使用 CBAM 注意力机制训练

```bash
python train_CIFAR10.py --prefix 5 --device 1 --epoch 160 --att_type cbam
```

### 验证结果

在 ResNet50 模型上训练了 160 个 epoch 后，验证结果如下：

- ACC@1 = 93.41%

## 注意事项

- 请确保在运行训练脚本前，已经正确配置了所需的环境。
- 训练过程中，请根据实际情况调整超参数，如 `--epoch` 和 `--device`。

## 贡献

欢迎大家提出改进建议或提交 Pull Request，共同完善这个项目。

## 下载链接

[ResNet_AttentionResNet注意力机制](https://pan.quark.cn/s/febae320fee1)