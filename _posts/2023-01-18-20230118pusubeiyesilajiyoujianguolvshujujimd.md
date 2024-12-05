---
layout: post
title: "朴素贝叶斯垃圾邮件过滤数据集"
date:   2024-01-07
tags: [spam,ham,垃圾邮件,texts,test]
comments: true
author: admin
---
# 朴素贝叶斯垃圾邮件过滤数据集

## 数据集说明

本仓库提供了一个用于朴素贝叶斯垃圾邮件过滤的数据集。数据集包含两个文件夹：

- **spam**：该文件夹下包含的是垃圾邮件的文本文件。
- **ham**：该文件夹下包含的是非垃圾邮件（正常邮件）的文本文件。

## 数据集格式

数据集中的每个邮件都以`.txt`文件的形式存储。每个文件的内容即为邮件的文本内容。

## 使用场景

该数据集适用于机器学习中的文本分类任务，特别是垃圾邮件过滤。你可以使用朴素贝叶斯分类器或其他分类算法来训练模型，以区分垃圾邮件和正常邮件。

## 如何使用

1. **克隆仓库**：首先，克隆本仓库到你的本地环境。
   ```bash
   git clone https://github.com/your-repo-url.git
   ```

2. **加载数据**：使用Python或其他编程语言加载数据集中的文本文件。
   ```python
   import os

   spam_folder = 'spam'
   ham_folder = 'ham'

   spam_files = os.listdir(spam_folder)
   ham_files = os.listdir(ham_folder)

   # 读取垃圾邮件
   spam_texts = [open(os.path.join(spam_folder, file), 'r').read() for file in spam_files]

   # 读取正常邮件
   ham_texts = [open(os.path.join(ham_folder, file), 'r').read() for file in ham_files]
   ```

3. **训练模型**：使用加载的数据训练你的分类模型。
   ```python
   from sklearn.feature_extraction.text import CountVectorizer
   from sklearn.naive_bayes import MultinomialNB
   from sklearn.model_selection import train_test_split

   # 合并数据
   texts = spam_texts + ham_texts
   labels = ['spam'] * len(spam_texts) + ['ham'] * len(ham_texts)

   # 向量化文本
   vectorizer = CountVectorizer()
   X = vectorizer.fit_transform(texts)

   # 划分训练集和测试集
   X_train, X_test, y_train, y_test = train_test_split(X, labels, test_size=0.2, random_state=42)

   # 训练朴素贝叶斯模型
   model = MultinomialNB()
   model.fit(X_train, y_train)

   # 评估模型
   accuracy = model.score(X_test, y_test)
   print(f'模型准确率: {accuracy:.2f}')
   ```

## 贡献

如果你有任何改进建议或发现了数据集中的问题，欢迎提交Issue或Pull Request。

## 许可证

本数据集遵循MIT许可证。你可以自由使用、修改和分发本数据集，但请保留原始的许可证声明。

---

希望这个数据集能帮助你在垃圾邮件过滤任务中取得良好的效果！

## 下载链接

[朴素贝叶斯垃圾邮件过滤数据集](https://pan.quark.cn/s/36b701c3c126)