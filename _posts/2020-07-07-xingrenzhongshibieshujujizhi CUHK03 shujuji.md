---
layout: post
title: "行人重识别数据集之 CUHK03 数据集"
date:   2022-03-22
tags: [行人,CUHK03,数据,包含,测试]
comments: true
author: admin
---
# 行人重识别数据集之 CUHK03 数据集

## 简介
CUHK03 数据集是行人重识别领域广泛使用的一个数据集，它的行人图片采集自香港中文大学（CUHK）校园的 5 对不同视角的摄像头。CUHK03 数据集有很多版本，包括 Matlab 文件格式和图片格式，不同版本的数据集可能包含不同数量的行人。

## 数据集版本
CUHK03 数据集有多种版本，主要分为以下两种格式：

### 1. Matlab 文件格式
- **cuhk03_release.zip**: 包含 Matlab 格式的文件 `cuhk-03.mat`，主要包含三个字段：
  - `detected`: 包含由行人检测器自动检测生成的边界框（行人图片）。
  - `labeled`: 包含人为手动标注的边界框（行人图片）。
  - `testsets`: 表示测试协议即数据集划分，测试集包括 100 个行人，重复 20 次。

### 2. 图片格式
- **CUHK03.tar.gz**: 包含 `detected` 文件夹和 `labeled` 文件夹，分别存储由行人检测器检测生成的行人图片和手动标注的行人图片。
- **CUHK03-NP 数据集**: 采用新的训练/测试协议进行划分的图片集，存储格式类似于 Market 1501 数据集。

## 数据集划分
CUHK03 数据集有两种主要的划分方式：

### 1. 经典划分
- 2014年提出的划分方式，数据集共包含 1360 个行人，训练集 1160 个行人，验证集 100 个行人，测试集 100 个行人。

### 2. 新的划分
- 2017年提出的新划分方式，数据集中共包含 1467 个行人，其中训练集中有 767 个行人，测试集中有 700 个行人。

## 使用说明
- **Matlab 文件格式**: 可以使用新的训练集/测试集协议，将两个 `.mat` 文件和 `cuhk03_release` 放在一起使用。
- **图片格式**: 数据集一般结合 `cuhk03.py` 生成的 json 文件一起使用，json 文件包含数据集划分信息。

## 参考文献
- DeepReID: Deep Filter Pairing Neural Network for Person Re-Identification
- Re-ranking person re-identification with k-reciprocal encoding

## 注意事项
- 不同代码用到的 CUHK03 数据集版本可能不同，使用时请注意版本兼容性。
- 数据集包含敏感数据，使用时应尊重中大学生的隐私。

## 下载链接

[行人重识别数据集之CUHK03数据集](https://pan.quark.cn/s/039fc5cc3763)