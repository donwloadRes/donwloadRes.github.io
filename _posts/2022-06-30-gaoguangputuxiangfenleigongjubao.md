---
layout: post
title: "高光谱图像分类工具包"
date:   2024-04-11
tags: [分类,代码,算法,光谱,classification]
comments: true
author: admin
---
# 高光谱图像分类工具包

## 简介

本仓库提供了一个用于高光谱图像分类的资源文件，包含了使用支持向量机（SVM）、随机森林（Random Forest）和K近邻（K-NN）算法进行分类的代码。此外，仓库中还内置了Indian_pines、PaviaU和Salinas三个常用的高光谱数据集及其对应的标签文件。

## 资源内容

- **代码文件**：
  - `svm_classification.py`：使用SVM算法进行高光谱图像分类的代码。
  - `random_forest_classification.py`：使用随机森林算法进行高光谱图像分类的代码。
  - `knn_classification.py`：使用K-NN算法进行高光谱图像分类的代码。

- **数据集**：
  - `Indian_pines.mat`：Indian Pines数据集及其标签。
  - `PaviaU.mat`：Pavia University数据集及其标签。
  - `Salinas.mat`：Salinas数据集及其标签。

## 使用说明

1. **数据集加载**：
   - 代码中已经内置了数据集的加载功能，用户可以直接使用这些数据集进行分类实验。

2. **算法选择**：
   - 用户可以根据需求选择使用SVM、随机森林或K-NN算法进行分类。
   - 每个算法的代码文件中都包含了详细的注释，方便用户理解和修改。

3. **结果输出**：
   - 代码会输出分类结果，并计算分类精度（Accuracy）。

## 依赖库

- Python 3.x
- scikit-learn
- numpy
- scipy
- matplotlib（用于可视化）

## 安装与运行

1. 克隆本仓库到本地：
   ```bash
   git clone https://github.com/your_username/your_repository.git
   ```

2. 安装依赖库：
   ```bash
   pip install -r requirements.txt
   ```

3. 运行分类代码：
   ```bash
   python svm_classification.py
   ```

## 贡献

欢迎对本仓库进行改进和扩展。如果您有任何建议或发现了问题，请提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[高光谱图像分类工具包](https://pan.quark.cn/s/20a0327c0483)