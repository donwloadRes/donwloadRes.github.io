---
layout: post
title: "Python实现OCR大批量识别图片文字并保存到txt文档"
date:   2021-04-01
tags: [识别,图片,txt,文字,Python]
comments: true
author: admin
---
# Python实现OCR大批量识别图片文字并保存到txt文档

## 项目简介
本项目使用Python实现OCR（光学字符识别）技术，能够大批量识别图片中的文字，并将识别结果保存到txt文档中。项目源码可以直接下载使用，适合需要进行图片文字识别和文本提取的用户。

## 项目背景
在当今数字化时代，图像文字识别（OCR）技术的应用越来越广泛。OCR技术可以将印刷体文字转化为可编辑的文本格式，从而方便进行文本分析、数据挖掘等操作。Python作为一种简洁、易用的编程语言，提供了丰富的图像处理和机器学习库，使得实现图像文字识别变得简单而高效。

## 项目功能
- **支持识别多种图片类型**：包括bmp、dib、jpeg、jpg、jpe、jp2、png、webp、pbm、pgm、pxm、pnm、tiff、tif等。
- **支持自定义图片路径**：用户可以指定图片的存放路径。
- **支持大批量的图片识别**：能够处理大量图片文件。
- **将每一张图片的文字写入对应的txt文件中**：识别结果会自动保存为txt文件。

## 运行环境
- Python 3.x
- 依赖库：paddlehub、cv2、os

## 运行步骤
1. **下载项目并解压到本地电脑**。
2. **配置运行环境**：使用pycharm导入项目，在【terminal】下运行以下命令安装依赖库：
   ```
   pip install -r requirements.txt
   ```
3. **运行前可以替换image_path为自定义的路径**，默认图片保存位置为当前py文件下的image文件夹。

## 代码详解
1. **导入需要的库**：paddlehub用于搭建模型，cv2用于读取图片，os模块创建文件。
2. **识别图片并保存识别结果**：传入图片地址，并将识别出的文字保存到对应的txt文本中。
3. **获取指定路径下的所有图片地址**：或者同级文件夹images中的所有图片地址。

## 源码地址
项目源码可以直接下载使用，具体下载地址请参考相关文档。

## 注意事项
- 本项目使用的文字识别模型来自飞桨开源模型：chinese_ocr_db_crnn_server。
- 该模型基于chinese_text_detection_db_server检测得到的文本框，继续识别文本框中的中文文字。
- 识别文字算法采用CRNN（Convolutional Recurrent Neural Network），即卷积递归神经网络。

## 联系我们
如有任何问题或建议，欢迎联系我们。

## 下载链接

[Python实现OCR大批量识别图片文字并保存到txt文档](https://pan.quark.cn/s/6007e6df8f6e)