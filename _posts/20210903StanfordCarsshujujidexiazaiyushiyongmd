---
layout: post
title: "Stanford Cars数据集的下载与使用"
date:   2023-01-10
tags: [class,annotations,下载,数据,类别]
comments: true
author: admin
---
# Stanford Cars数据集的下载与使用

## 简介

Stanford Cars数据集是一个用于细粒度分类任务的数据集，包含16185张不同型号的汽车图片。其中，8144张为训练集，8041张为测试集。该数据集主要用于区分不同品牌、型号和年份的汽车。

## 数据集内容

- **图片数量**: 16185张
- **训练集**: 8144张
- **测试集**: 8041张
- **类别数量**: 196类

## 下载方式

数据集可以通过以下方式下载：

1. **官网下载**: 访问Stanford Cars数据集的官方网站进行下载。
2. **百度网盘下载**: 如果官网链接失效，可以通过百度网盘下载，提取码为6666。

## 数据集结构

数据集包含两个主要文件：

1. **图片文件夹**: 包含所有16185张汽车图片。
2. **标注文件**: 以MATLAB格式保存的标注文件，包含图片的类别、边界框等信息。

## 使用方法

### 1. 提取类别名

使用Python脚本提取类别名，并保存为文本文件。

```python
import scipy.io

data = scipy.io.loadmat('cars_annos.mat')
class_names = data['class_names']

with open('label_map.txt', 'w') as f_class:
    for j in range(class_names.shape[1]):
        class_name = str(class_names[0, j][0]).replace(' ', '_')
        f_class.write(f"{j+1} {class_name}\n")
```

### 2. 提取图片信息

提取图片的序号、文件名、类别和是否属于测试集的信息。

```python
import scipy.io

data = scipy.io.loadmat('cars_annos.mat')
annotations = data['annotations']

with open('mat2txt.txt', 'w') as f_train:
    for i in range(annotations.shape[1]):
        name = str(annotations[0, i][0])[2:-2]
        test = int(annotations[0, i][6])
        clas = int(annotations[0, i][5])
        f_train.write(f"{i+1} {name} {clas} {test}\n")
```

## 注意事项

- 在提取类别名时，如果类别名中包含斜杠（/），建议将其替换为下划线（_），以避免读取文件时出错。
- 数据集大小约为2GB，建议在Linux系统下使用axel多线程下载工具进行下载，以提高下载速度并支持断点续传。

## 参考资料

该数据集的使用方法和详细介绍可以参考CSDN博客文章《Stanford Cars数据集的下载与使用》。

## 下载链接

[StanfordCars数据集的下载与使用](https://pan.quark.cn/s/bb4a1c99ac74)