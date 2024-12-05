---
layout: post
title: "Keras人脸识别模型"
date:   2020-01-22
tags: [facenet,人脸,人脸识别,face,keras]
comments: true
author: admin
---
# Keras人脸识别模型

## 简介

这是一个基于mtcnn和facenet的人脸识别模型，可实现在线人脸识别。该模型使用Keras框架实现，能够有效地进行人脸检测和对齐，并通过facenet提取人脸特征进行识别。

## 目录结构

- `face_dataset/`: 存放待识别的人脸数据集。
- `model_data/`: 存放模型权重文件，包括`facenet_keras.h5`。
- `net/`: 存放网络结构文件。
- `result/`: 存放识别结果。
- `utils/`: 存放工具函数。
- `LICENSE`: 许可证文件。
- `README.md`: 项目说明文件。
- `align.py`: 人脸对齐脚本。
- `face_recognize.py`: 人脸识别主脚本。

## 所需环境

- tensorflow-gpu==1.13.1
- keras==2.1.5

## 文件下载

训练所需的`facenet_keras.h5`文件可以在Release中下载，也可以通过百度网盘下载。

## 使用方法

1. 先将整个仓库download下来。
2. 下载完之后解压，同时下载`facenet_keras.h5`文件。
3. 将`facenet_keras.h5`放入`model_data`中。
4. 将自己想要识别的人脸放入到`face_dataset`中。
5. 运行`face_recognize.py`即可。
6. `align.py`可以查看人脸对齐的效果。

## 效果

`face_recognize.py`的运行结果将显示识别出的人脸及其对应的身份信息。

## 下载链接

[Keras人脸识别模型分享](https://pan.quark.cn/s/ed6908bd4ef7)