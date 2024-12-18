---
layout: post
title: "常见公开人脸数据集的获取和制作自定义人脸数据集"
date:   2022-09-23
tags: [人脸,图片,数据,人脸识别,自定义]
comments: true
author: admin
---
# 常见公开人脸数据集的获取和制作自定义人脸数据集

本文介绍了如何获取常见公开的人脸数据集以及如何制作自定义的人脸数据集。人脸数据集在开发人脸识别系统时是必不可少的，因此本文将详细介绍从公开数据集到自制数据集的整个过程，为后续开发人脸识别系统做好准备。

## 公开人脸数据集

本文介绍了几个人脸数据集，包括CelebA、LFW、WIDER和emore数据集。每个数据集都有其特定的用途和特点，例如CelebA数据集包含了大量的人脸图片和详细的标注信息，而LFW数据集则主要用于人脸识别的评估。

### CelebA人脸数据集

CelebA数据集包含了大量经过对齐和裁剪的人脸图片，每张图片都有详细的标注信息，包括人脸属性、人脸位置和人脸关键点等。

### LFW数据集

LFW数据集是一个广泛使用的人脸识别数据集，包含了大量的人脸图片和对应的标注信息，主要用于评估人脸识别算法的性能。

### WIDER人脸数据集

WIDER数据集包含了大量的人脸图片，每张图片可能包含多个人脸，标注信息包括每个人脸的位置和大小。

### emore数据集

emore数据集是一个大规模的人脸识别数据集，包含了大量的人脸图片，每张图片都有对应的标注信息。

## 制作自定义人脸数据集

本文还介绍了如何制作自定义的人脸数据集。制作自定义人脸数据集的过程可以分为两个阶段：第一阶段是人脸图片的获取和简单的清洗，第二阶段是人脸图片的高级清洗和标注人脸信息。

### 第一阶段：人脸图片的获取和清洗

在第一阶段，我们首先通过网络爬虫获取人脸图片，然后删除损坏的图片和没有包含人脸的图片，或者包含过多人脸的图片。

### 第二阶段：高级清洗和标注

在第二阶段，我们选择每个文件夹中包含相同一个人的图片，选择其中一个作为主人脸图片，然后使用这个主图片来对比其他图片，判断是否是同一个人。如果不是，就删除该图片。最后，使用百度的人脸检测服务标注清理后的图片，最终得到一个人脸数据集。

通过本文的介绍，读者可以了解到如何获取和制作自定义的人脸数据集，为开发人脸识别系统打下坚实的基础。

## 下载链接

[常见公开人脸数据集的获取和制作自定义人脸数据集](https://pan.quark.cn/s/1109a3f8d100)