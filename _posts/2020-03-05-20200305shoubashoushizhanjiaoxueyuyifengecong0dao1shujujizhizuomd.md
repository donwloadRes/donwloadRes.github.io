---
layout: post
title: "手把手实战教学语义分割从0到1  数据集制作"
date:   2024-03-03
tags: [标注,语义,分割,VOC,数据]
comments: true
author: admin
---
# 手把手实战教学：语义分割从0到1 - 数据集制作

本资源文件是《手把手实战教学：语义分割从0到1》系列的第一篇实战教学，重点介绍语义分割相关数据集的制作方法。通过本教程，您将学习如何准备标注工具、原始数据，并进行标注，最终将标注数据转换为VOC格式，以便用于语义分割模型的训练。

## 内容概述

### 1. 公开数据集
常用的语义分割数据集包括COCO、VOC、Cityscapes、ADE20K等。作为入门，建议从VOC和COCO开始了解，大多数开源框架也会支持这两种数据集。

### 2. 制作自己的语义分割数据集
#### 2.1 准备标注工具
使用标注工具labelme进行图像标注。可以通过pip安装labelme，并查看帮助信息。

#### 2.2 准备待标注的原始数据
原始数据应为图片格式，建议统一存放在一个文件夹中，并创建一个文件夹用于存放标注后的json文件。同时，创建一个TXT文档（labels.txt）用于指明标注的类别。

#### 2.3 开始标注
使用labelme工具对图片进行标注，生成对应的json文件。

#### 2.4 标注界面
标注界面与labelimg类似，用户可以通过界面逐点勾勒出目标的轮廓。

#### 2.5 转为VOC格式
标注完成后，使用labelme自带的脚本将标注数据转换为VOC格式，生成与VOC数据集一致的目录结构。

### 3. 写在后面
完成数据集制作后，即可利用转化后的数据集进行语义分割模型的训练。

通过本教程，您将掌握从数据集制作到模型训练的全过程，为后续的语义分割实战打下坚实基础。

## 下载链接

[手把手实战教学语义分割从0到1-数据集制作](https://pan.quark.cn/s/97c1823d4a42)