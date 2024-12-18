---
layout: post
title: "Yolo v570版本中文标签显示方法"
date:   2024-07-10
tags: [标签,中文,Yolo,v5,7.0]
comments: true
author: admin
---
# Yolo v5-7.0版本中文标签显示方法

本文详细介绍了如何在Yolo v5-7.0版本中实现中文标签的显示方法，并附带了所需字体的下载链接。通过本文的指导，您可以轻松地将Yolo v5-7.0的目标识别结果中的标签显示为中文。

## 前提条件

1. 本文适用于Yolo v5-7.0版本，其他版本可能不适用，请自行尝试。
2. 本文假设您在训练时使用的是英文标签，只是在标记层面将英文标签用中文显示。如果您已经使用中文训练，则无需继续阅读。

## 实现步骤

### 1. 查看标记源码

在Yolo v5的源代码中，标记相关的源代码位于`utils`文件夹中的`plots.py`文件中。打开该文件后，找到`class Annotator`这个类函数，将其中的字体改为中文字体（绝对路径），并将`pil=False`改为`True`。

### 2. 修改detect代码

由于我们是在标记层面使用中文标签，因此在源代码中还需要将训练时的英文标签和中文对应起来。最简单的办法是创建一个字典，例如：

```python
dict_label = {"Dog": "狗", "Cat": "猫"}
```

然后在程序写入标签的地方将标签替换掉。具体操作如下：

1. 找到原始的`label`，它返回的数据格式为“Dog 0.55”，即类别+可信度。
2. 使用字典将英文标签替换为中文标签，例如：`dict_label[label[:-5]]`。
3. 将替换后的标签传递给`annotator.box_label`函数。

### 3. 字体文件

为了实现中文标签的显示，您需要下载中文字体文件，并将其路径添加到源代码中。您可以从“C:\Windows\Fonts”中选择一个中文字体，或者使用本文提供的字体链接进行下载。

## 总结

通过以上步骤，您可以成功在Yolo v5-7.0版本中实现中文标签的显示。如果您在操作过程中遇到任何问题，欢迎留言讨论。

## 下载链接

[Yolov5-7.0版本中文标签显示方法](https://pan.quark.cn/s/7ed0b93bc6f0)