---
layout: post
title: "人脸表情识别——基于Hog特征与基本分类算法的Python实现"
date:   2022-08-10
tags: [表情,Hog,Python,JAFFE,特征提取]
comments: true
author: admin
---
# 人脸表情识别——基于Hog特征与基本分类算法的Python实现

## 项目简介

本项目提供了一个基于Hog特征和多种基本分类算法的人脸表情识别Python实现。通过使用日本女性面部表情数据库（JAFFE），本项目实现了对七种基本表情（sad, happy, angry, disgust, surprise, fear, neutral）的分类。

## 主要功能

1. **数据读取与预处理**：
   - 从JAFFE数据库中读取图像数据，并进行归一化处理。
   - 将数据集分为训练集和测试集。

2. **Hog特征提取**：
   - 对训练集和测试集中的图像进行Hog特征提取。

3. **分类算法实现**：
   - 支持向量机（SVM）
   - K近邻算法（KNN）
   - 朴素贝叶斯（Naive Bayes）
   - 随机森林（Random Forest）
   - 逻辑回归（Logistic Regression）
   - 决策树（Decision Tree）

4. **模型评估**：
   - 计算分类模型的准确度、召回率和混淆矩阵。

5. **表情预测**：
   - 使用训练好的模型对新图像进行表情预测。

## 使用方法

1. **数据准备**：
   - 下载JAFFE数据库，并将其放置在指定目录下。

2. **运行代码**：
   - 运行提供的Python脚本，进行数据读取、特征提取、模型训练和评估。

3. **表情预测**：
   - 使用训练好的模型对新图像进行表情预测。

## 依赖库

- Python 3.x
- OpenCV
- scikit-learn
- numpy
- matplotlib
- seaborn

## 参考文献

- 特征提取：HOG
- KNN参考
- SVM参考

## 致谢

感谢JAFFE数据库的提供者，以及所有开源库的贡献者。

## 注意事项

- 本项目为初学者实践项目，代码和文章如有不足之处，敬请指正。
- 本项目仅供学习和研究使用，请勿用于商业用途。

## 下载链接

[人脸表情识别基于Hog特征与基本分类算法的Python实现](https://pan.quark.cn/s/4cc6b940f02d)