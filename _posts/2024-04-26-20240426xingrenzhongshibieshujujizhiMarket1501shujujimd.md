---
layout: post
title: "行人重识别数据集之 Market1501 数据集"
date:   2020-05-12
tags: [行人,图片,Market1501,训练,数据]
comments: true
author: admin
---
# 行人重识别数据集之 Market1501 数据集

## 简介
Market1501 数据集是行人重识别领域的重要资源，由6个摄像头捕获的1501个行人的图片组成。数据集分为训练集、测试集和query集，用于模型训练和评估。每个行人图片命名包含行人ID、摄像头编号、视频片段和帧信息。数据集结构包括训练图片、测试图片、手工标注图片和查询信息，用于模型训练和行人检索。

## 数据集结构
- **训练集**：包含751个行人，共计12936张图片。
- **测试集**：包含750个行人，共计19732张图片。
- **query集**：包含750个行人，共计3368张图片。

## 数据集命名规则
以图片 `0012_c4s1_000826_01.jpg` 为例：
- `0012`：行人ID，Market1501 有 1501 个行人，故行人 ID 范围为 0001-1501。
- `c4`：摄像头编号，表明图片采集自第4个摄像头，一共有 6 个摄像头。
- `s1`：视频的第一个片段，一个视频包含若干个片段。
- `000826`：视频的第 826 帧图片，表明行人出现在该帧图片中。
- `01`：代表第 826 帧图片上的第一个检测框，DPM 检测器可能在一帧图片上生成多个检测框。

## 使用说明
1. **训练模型**：使用训练集进行模型训练。
2. **测试模型**：使用测试集和query集进行模型评估。
3. **行人检索**：利用query集进行行人检索任务。

## 注意事项
- 数据集下载后，请确保遵守相关的许可和使用条款。
- 使用数据集前，建议阅读官方提供的文档和指南，以获取更多关于数据集的详细信息和使用说明。

## 参考文献
Market1501 数据集由清华大学在2015年提出，论文标题为 "Person Re-Identification Meets Image Search"。

## 下载链接

[行人重识别数据集之Market1501数据集分享](https://pan.quark.cn/s/2342365b4409)