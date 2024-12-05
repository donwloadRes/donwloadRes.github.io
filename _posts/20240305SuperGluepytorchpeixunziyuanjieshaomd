---
layout: post
title: "SuperGlue-pytorch培训资源介绍"
date:   2024-02-20
tags: [--,训练,SuperGlue,资源,pytorch]
comments: true
author: admin
---
# SuperGlue-pytorch培训资源介绍

## 资源描述

本仓库提供了一个名为“SuperGlue-pytorch培训”的资源文件，该资源文件是基于官方超点实现的改编版本，主要包含以下几个改进和功能：

1. **基于官方超点实现**：本资源文件基于官方的超点实现进行改编，确保了代码的可靠性和准确性。

2. **启用训练batchsize > 1**：通过优化代码，使得训练时可以支持大于1的batchsize，提高了训练效率。

3. **损失前进速度10倍加速**：对损失计算进行了优化，使得训练过程中的损失前进速度提升了10倍，大大缩短了训练时间。

4. **启用训练集非线性扭曲**：在训练集中启用了非线性扭曲，增加了数据的多样性，有助于模型更好地泛化。

5. **训练集中的负对**：在训练集中引入了负对样本，帮助模型更好地学习区分不同样本。

6. **启用离线数据生成**：支持离线数据生成，可以通过以下命令构建训练集：
   ```bash
   python -m dataset.data_builder --debug 1
   ```

## 训练命令

使用以下命令进行训练：
```bash
python train.py --train_path {train_path} --superpoint_weight ./models/weights/superpoint_v1.pth --feature_dim 256 --dataset_offline_rebuild 1 --pretrained --batch_size 32 --debug 0
```

## 依赖关系

本资源文件依赖于Python 3环境。

## 其他说明

本资源文件还附带了SuperGlue PyTorch实施的全文PDF，供用户参考。

## 下载链接

[SuperGlue-pytorch培训资源介绍](https://pan.quark.cn/s/7937b85551c2)