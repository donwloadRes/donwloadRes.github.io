---
layout: post
title: "UEA多元时间序列数据集（CSV格式）"
date:   2024-11-23
tags: [csv,数据,test,train,label]
comments: true
author: admin
---
# UEA多元时间序列数据集（CSV格式）

## 简介

本仓库提供了一个名为“UEA多元时间序列数据集”的资源文件，该数据集以CSV格式存储，适用于多元时间序列数据的分析和处理。数据集将多元时间序列数据的多维特性拆解成多个一维文件，便于用户进行进一步的数据处理和分析。

## 数据集结构

数据集的存储结构如下：

```
E:/桌面/代码/数据集/Multivariate2018_arff_csv
    - ArticularyWordRecognition
        - test_dim1.csv
        - test_dim2.csv
        ...
        - train_dim1.csv
        - train_dim2.csv
        ...
        - train_label.csv
        - test_label.csv
```

每个数据集文件夹下包含以下内容：

- **测试集数据**：以`test_dimX.csv`命名，其中`X`表示数据的维度。
- **测试集标签**：以`test_label.csv`命名。
- **训练集数据**：以`train_dimX.csv`命名，其中`X`表示数据的维度。
- **训练集标签**：以`train_label.csv`命名。

## 使用说明

1. **下载数据集**：您可以通过本仓库提供的下载链接获取数据集文件。
2. **数据处理**：根据您的需求，使用相应的工具或编程语言（如Python、R等）读取CSV文件，进行数据处理和分析。
3. **数据集应用**：该数据集适用于多元时间序列数据的分类、聚类、预测等任务。

## 注意事项

- 数据集文件较大，建议在下载和处理时确保有足够的存储空间和计算资源。
- 数据集的标签文件（`train_label.csv`和`test_label.csv`）提供了每个样本的类别信息，请在模型训练和评估时使用。

## 贡献

如果您在使用过程中发现任何问题或有改进建议，欢迎提交Issue或Pull Request。

## 许可证

本数据集遵循特定的许可证，请在使用前仔细阅读相关许可证条款。

---

希望本数据集能够帮助您在多元时间序列数据分析方面取得进展！

## 下载链接

[UEA多元时间序列数据集CSV格式](https://pan.quark.cn/s/fe309db0cd83)