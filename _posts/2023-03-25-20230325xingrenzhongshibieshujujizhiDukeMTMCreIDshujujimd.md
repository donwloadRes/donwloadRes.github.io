---
layout: post
title: "行人重识别数据集之 DukeMTMC-reID 数据集"
date:   2020-03-26
tags: [数据,reID,DukeMTMC,图像,行人]
comments: true
author: admin
---
# 行人重识别数据集之 DukeMTMC-reID 数据集

## 简介
DukeMTMC-reID 数据集是 2017 年发布的一个大规模行人重识别图片数据集，它采集于 Duke 大学校园的 8 个静态摄像头。该数据集现已被广泛使用，学术界和工业界提出的行人重识别（reID）算法模型都会使用它作为数据集。

## 数据集结构
DukeMTMC-reID 数据集依照 Market 1501 数据集的结构进行组织，主要包括以下三个子集：
- **bounding_box_test**: 画廊图像，用于从图像池中检索查询。
- **bounding_box_train**: 训练图像，包含来自 702 个不同身份的图像。
- **query**: 查询图像，每个图像来自不同摄像头中的不同身份。

## 数据集命名规则
数据集中的图像命名规则如下：
- **0014_c2_f0053184.jpg**:
  - **0014**: 行人 ID 编号。
  - **c2**: 表示图片采集自第二个摄像头。
  - **f0053184**: 表示图片是摄像头 2 的第 53184 帧。

## 数据集下载
该资源文件提供了 DukeMTMC-reID 数据集的下载链接，用户可以通过下载链接获取数据集的压缩文件。

## 参考文献
- Unlabeled Samples Generated by GAN Improve the Person Re-identification Baseline in vitro
- Performance Measures and a Data Set for Multi-Target, Multi-Camera Tracking

## 使用说明
用户在下载并解压数据集后，可以按照数据集的结构进行训练和测试。数据集的详细使用方法可以参考相关文献和行人重识别算法的实现代码。

## 注意事项
使用该数据集时，请遵守相关的版权声明和使用条款，仅用于非商业研究和教育目的。

## 下载链接

[行人重识别数据集之DukeMTMC-reID数据集分享](https://pan.quark.cn/s/c89c502c753e)