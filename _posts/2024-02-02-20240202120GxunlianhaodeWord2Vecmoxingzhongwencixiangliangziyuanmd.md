---
layout: post
title: "120G训练好的Word2Vec模型中文词向量资源"
date:   2023-04-08
tags: [模型,model,向量,中文,Word2Vec]
comments: true
author: admin
---
# 120G+训练好的Word2Vec模型（中文词向量资源）

## 简介

本资源提供了一个经过大规模语料训练的Word2Vec模型，专门用于中文词向量的生成。该模型基于268G+的语料数据进行训练，涵盖了百度百科、搜狐新闻、小说等多种类型的文本数据。通过使用该模型，用户可以轻松地生成高质量的中文词向量，适用于自然语言处理（NLP）中的各种任务，如文本分类、情感分析、机器翻译等。

## 模型参数

- **window**: 5
- **min_count**: 10
- **size**: 128
- **hs**: 1
- **negative**: 0
- **iter**: 5

## 使用方法

### 1. 加载bin模型

```python
import gensim
model = gensim.models.KeyedVectors.load_word2vec_format('model.bin', binary=True)
print(model['love'])
```

### 2. 加载model模型

```python
model = gensim.models.Word2Vec.load('model_path')
```

## 训练语料

- 百度百科：800w+条，26G+
- 搜狐新闻：400w+条，13G+
- 小说：229G+

## 其他说明

- 分词词典使用了130w+词典，分词代码：`jieba.lcut(sentence)`，默认使用了HMM识别新词。
- 剔除了所有非中文字符。
- 最终得到的词典大小为6115353。

## 适用场景

该模型适用于需要高质量中文词向量的各种NLP任务，如：

- 文本分类
- 情感分析
- 机器翻译
- 信息检索
- 问答系统
- 文本相似度计算
- 文本聚类
- 信息抽取

## 注意事项

- 请确保在使用模型前安装了`gensim`库。
- 模型文件较大，建议在有足够内存的机器上使用。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有任何建议，欢迎通过GitHub Issues进行反馈。我们非常乐意听取您的意见，并不断改进模型。

## 关键词

- Word2Vec
- 中文词向量
- 自然语言处理
- NLP
- 机器学习
- 深度学习

## 下载链接

[120G训练好的word2vec模型中文词向量分享](https://pan.quark.cn/s/880afb03862e)