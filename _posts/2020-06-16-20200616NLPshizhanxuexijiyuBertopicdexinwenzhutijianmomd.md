---
layout: post
title: "NLP实战学习：基于Bertopic的新闻主题建模"
date:   2024-11-22
tags: [Bertopic,主题,建模,预处理,NLP]
comments: true
author: admin
---
# NLP实战学习：基于Bertopic的新闻主题建模

本仓库提供了一个资源文件，用于支持NLP实战学习中的新闻主题建模任务。该资源文件基于Bertopic模型，旨在帮助用户理解和实践如何使用Bertopic进行新闻主题的自动建模。

## 资源文件内容

- **数据集**：包含250万篇新闻数据，原始数据大小为9GB，压缩文件大小为3.6GB。新闻内容跨度为2014-2016年，涵盖了6.3万个媒体。
- **数据格式**：json格式，包含标题、正文、关键词、描述和来源等信息。
- **预处理脚本**：提供数据预处理脚本，包括读取json文件、分词、去除标点符号等操作，最终将数据存入CSV文件。

## 使用说明

1. **数据预处理**：
   - 解压数据文件。
   - 使用提供的预处理脚本对数据进行分词和去除停用词等操作。

2. **主题建模**：
   - 导入必要的库，如Bertopic、SentenceTransformer等。
   - 读取预处理后的数据，进行句子嵌入和降维处理。
   - 使用HDBSCAN进行文档聚类，并通过c-TF-IDF提取主题关键词。

3. **结果分析**：
   - 查看每个主题下的TOP主题词。
   - 进行主题归并，优化主题模型。

## 依赖库

- Python 3.x
- Bertopic
- SentenceTransformer
- UMAP
- HDBSCAN
- scikit-learn
- pandas
- jieba

## 参考文献

- [BERTopic: Neural topic modeling with a class-based TF-IDF procedure](https://arxiv.org/abs/2203.05794)

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个资源文件。

## 许可证

本项目遵循CC 4.0 BY-SA版权协议。

## 下载链接

[NLP实战学习基于Bertopic的新闻主题建模](https://pan.quark.cn/s/22744df5d990)