---
layout: post
title: "不可思议的Word2Vec训练好的模型"
date:   2021-06-30
tags: [模型,语料,Word2Vec,训练,微信]
comments: true
author: admin
---
# 不可思议的Word2Vec：训练好的模型

## 简介

本资源文件提供了一个经过训练的Word2Vec模型，该模型基于微信公众号文章的多领域中文平衡语料进行训练。模型包含了352196个词汇，使用Skip-Gram + Huffman Softmax结构，向量维度为256维。该模型适用于中文文本处理任务，如词向量生成、近义词查找等。

## 模型概况

- **训练语料**：微信公众号文章，多领域，属于中文平衡语料
- **语料数量**：800万篇，总词数达到650亿
- **模型词数**：共352196词，基本是中文词，包含常见英文词
- **模型结构**：Skip-Gram + Huffman Softmax
- **向量维度**：256维
- **分词工具**：结巴分词，加入了有50万词条的词典，关闭了新词发现
- **训练工具**：Gensim的Word2Vec，服务器训练了7天
- **其他情况**：窗口大小为10，最小词频是64，迭代了10次

## 使用说明

1. **加载模型**：使用Gensim库加载模型文件。
2. **词向量生成**：通过模型获取词汇的词向量。
3. **近义词查找**：使用模型查找与指定词汇相近的词汇。

## 示例代码

```python
import gensim

# 加载模型
model = gensim.models.Word2Vec.load('word2vec_wx')

# 查找近义词
similar_words = model.most_similar(u'微信')
print(similar_words)
```

## 注意事项

- 该模型适用于中文文本处理任务，建议在类似语料环境下使用。
- 模型的训练语料主要来自微信公众号文章，因此对于其他类型的文本可能效果有所不同。

## 下载链接

请访问原始文章获取下载链接。

## 参考文献

- [不可思议的Word2Vec：训练好的模型](https://blog.csdn.net/cjjwwss/article/details/80330156)

## 下载链接

[不可思议的Word2Vec训练好的模型分享](https://pan.quark.cn/s/942ba34ffaf1)