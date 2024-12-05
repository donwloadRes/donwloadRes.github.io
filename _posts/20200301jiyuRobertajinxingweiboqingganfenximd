---
layout: post
title: "基于Roberta进行微博情感分析"
date:   2023-03-09
tags: [Roberta,微博,Transformers,模型,训练]
comments: true
author: admin
---
# 基于Roberta进行微博情感分析

## 概述
本资源文件提供了一个基于Roberta模型的微博情感分析实现。该实现使用了预训练的Roberta-wwm-ext模型，对微博数据进行情感分类，共分为六种类别：积极、愤怒、悲伤、恐惧、惊奇和无情绪。

## 数据介绍
- **训练集**：包含27,768条微博数据。
- **测试集**：包含5,000条微博数据。

数据格式如下：
- `id`：编号
- `content`：文本内容
- `label`：情绪标签

## 模型训练
本实现基于HuggingFace开源的Transformers库（Torch版本）进行模型训练。主要库版本如下：
- Transformers == 2.2.2
- Torch == 1.5.0

### 加载预训练模型
使用RoBERTa-wwm-ext模型进行预训练，模型参数通过全连接层转换为六种情感分类的输出。

### 构造训练数据和测试数据
数据经过token化处理后，生成三类向量：
1. 文本本身的token
2. 表征token type的向量
3. 表示mask标志的向量

### 训练过程
- **机器配置**：两张V100 GPU
- **batch_size**：8
- 每个epoch耗时约6分钟，训练了3个epoch。

## 测试结果
测试结果显示，总体精度为78.02%。展示了20条测试结果，初步认为该模型可以作为一个基础模型使用。

## 使用方法
1. 安装依赖：`npm install -g architect-local @architect/architect`
2. 运行训练脚本：`python train.py`
3. 运行测试脚本：`python testCase.py`

## 参考文献
- 本文参考了HuggingFace开源的Transformers库和相关文献。

## 写在后面
- 个人认为HuggingFace开源的Transformers比较成功，值得国内同行学习。
- 完整代码可在资源文件中找到。

## 下载链接

[基于Roberta进行微博情感分析](https://pan.quark.cn/s/f9246c849d66)