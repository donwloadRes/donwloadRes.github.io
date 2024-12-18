---
layout: post
title: "SAR遥感图像舰船数据集"
date:   2023-04-16
tags: [格式,YOLO,XML,标注,图像]
comments: true
author: admin
---
# SAR遥感图像舰船数据集

## 简介

本仓库提供了一个SAR遥感图像舰船数据集，适用于目标检测任务。数据集已按照YOLO格式和XML格式进行标注，并已随机按照6:2:2的比例划分好训练集、验证集和测试集。

## 数据集内容

- **格式**：数据集包含两种标注格式，分别是YOLO格式和XML格式。
- **划分**：数据集已随机按照60%训练集、20%验证集和20%测试集的比例进行划分。
- **适用任务**：适用于SAR遥感图像中的舰船目标检测任务。

## 使用说明

1. **下载数据集**：请从本仓库下载数据集文件。
2. **数据集结构**：
   - `train/`：包含训练集图像及其对应的YOLO和XML标注文件。
   - `val/`：包含验证集图像及其对应的YOLO和XML标注文件。
   - `test/`：包含测试集图像及其对应的YOLO和XML标注文件。
3. **标注格式**：
   - YOLO格式：适用于YOLO系列目标检测模型。
   - XML格式：适用于其他需要XML标注的目标检测模型。

## 注意事项

- 数据集已进行随机划分，确保训练集、验证集和测试集的独立性。
- 请根据具体任务需求选择合适的标注格式进行使用。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有任何建议，欢迎提交Issue或Pull Request。我们期待您的反馈，以便不断改进数据集的质量和可用性。

## 下载链接

[SAR遥感图像舰船数据集](https://pan.quark.cn/s/a19679d282e6)