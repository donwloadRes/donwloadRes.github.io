---
layout: post
title: "目标跟踪UAV123数据集下载及使用指南"
date:   2024-02-08
tags: [UAV123,下载,数据,视频,OTB]
comments: true
author: admin
---
# 目标跟踪UAV123数据集下载及使用指南

## 简介
本仓库提供了一个用于目标跟踪的UAV123数据集的下载资源。UAV123数据集是一个专门由无人机拍摄的场景数据集，特点是背景干净，视角变化较多。该数据集包含123个短视频，总大小约为13.5GB。本指南将详细介绍如何下载和使用该数据集。

## 数据集内容
- **UAV123**: 包含123个短视频，每个视频都有详细的标注信息。
- **UAV20L**: 包含20个长视频，同样有详细的标注信息。

## 下载方式
1. **下载渠道1**: 访问UAV123数据集主页进行下载。
2. **下载渠道2**: 使用百度网盘下载，提取码为`7lwk`。网盘中包含5个压缩包，一起解压即可。

## 使用指南
### 主要文件
- **anno文件夹**: 包含UAV20L和UAV123的groundtruth标注，格式为左上角坐标和长宽四个值一行/帧。
- **data_seq文件夹**: 包含数据集的所有图片文件，命名方式为`06i.jpg`。
- **configSeqs.m文件**: 模仿OTB工具的视频信息文件，用于简单的跑库。

### 预处理
1. 下载并解压数据集。
2. 使用`utils_UAV.m`文件进行预处理，生成OTB数据集格式的frame文件。

### 跑库与评测
1. **跑库**: 以ECO为例，跑ECO-HC跟踪算法。设置方法与SRDCF算法类似。
2. **评测**: 评测主要指标是AUC和精度，与OTB报告的指标一致。

## 注意事项
- UAV的视频部分有目标完全离开视野的情况，这种情况的groundtruth标注为`NaN`，评测时需剔除这些帧。
- 本方法不限于UAV库，OTB和VOT数据集也适用。

## 联系我们
如有任何问题或建议，欢迎通过GitHub Issues联系我们。

## 下载链接

[目标跟踪UAV123数据集下载及使用指南](https://pan.quark.cn/s/72adb077d3a1)