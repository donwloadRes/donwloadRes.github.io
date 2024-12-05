---
layout: post
title: "GCN节点分类Cora数据集"
date:   2021-12-29
tags: [节点,Cora,GCN,数据,data]
comments: true
author: admin
---
# GCN节点分类Cora数据集

## 简介
本仓库提供了一个用于GCN（图卷积网络）节点分类任务的Cora数据集。Cora数据集是一个经典的图数据集，广泛用于图神经网络的研究和实验。该数据集包含了科学论文的引用网络，节点代表论文，边代表引用关系。每个节点还附带了论文的特征向量，用于节点分类任务。

## 数据集描述
- **节点数量**：2708
- **边数量**：5429
- **特征维度**：1433
- **类别数量**：7

## 文件结构
- `cora.content`: 包含节点特征和标签的文件。每行代表一个节点，格式为：`节点ID 特征向量 标签`。
- `cora.cites`: 包含边信息的文件。每行代表一条边，格式为：`节点ID1 节点ID2`。

## 使用方法
1. **下载数据集**：直接下载本仓库中的`cora.content`和`cora.cites`文件。
2. **加载数据集**：使用Python或其他编程语言加载数据集，进行GCN模型的训练和测试。

## 示例代码
以下是一个简单的Python代码示例，展示如何加载Cora数据集并进行GCN模型的训练。

```python
import numpy as np
import scipy.sparse as sp
import torch
from torch_geometric.datasets import Planetoid

# 加载Cora数据集
dataset = Planetoid(root='./data/Cora', name='Cora')
data = dataset[0]

# 打印数据集信息
print(f'节点数量: {data.num_nodes}')
print(f'边数量: {data.num_edges}')
print(f'特征维度: {data.num_node_features}')
print(f'类别数量: {data.num_classes}')

# 训练GCN模型
# ...
```

## 注意事项
- 数据集已经预处理，可以直接用于GCN模型的训练。
- 在使用数据集时，请确保遵循相关的使用许可和版权规定。

## 贡献
欢迎对本仓库进行贡献，包括但不限于数据集的改进、代码优化等。请提交Pull Request或Issue进行讨论。

## 许可证
本仓库中的数据集遵循MIT许可证。详细信息请参阅`LICENSE`文件。

## 下载链接

[GCN节点分类Cora数据集](https://pan.quark.cn/s/23c4de56e54c)