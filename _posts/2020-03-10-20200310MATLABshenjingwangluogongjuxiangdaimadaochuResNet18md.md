---
layout: post
title: "MATLAB神经网络工具箱代码导出 - ResNet18"
date:   2021-10-12
tags: [MATLAB,224,网络,图像,ResNet]
comments: true
author: admin
---
# MATLAB神经网络工具箱代码导出 - ResNet18

## 描述

本资源文件提供了将MATLAB神经网络工具箱代码导出为ResNet-18的功能。ResNet-18是一个卷积神经网络，它在来自ImageNet数据库的超过一百万张图像上进行了训练。通过训练，网络已经为各种图像学习了丰富的特征表示。该网络可以将图像分为1000个对象类别，例如键盘、鼠标、铅笔和许多动物。该网络的图像输入大小为224×224×3。

## 使用方法

此存储库需要MATLAB（R2018b及更高版本）和深度学习工具箱。该存储库提供以下三个功能：

### 1. `resnet18Layers`

使用ResNet-18的网络架构创建未经训练的网络。要从头开始训练网络，请在MATLAB命令行中键入以下内容：

```matlab
lgraph = resnet18Layers;
```

未经训练的网络将作为`layerGraph`对象返回。

### 2. `assembleResNet18`

要构建适用于图像分类的经过训练的ResNet-18网络，请在MATLAB命令行中键入以下内容：

```matlab
net = assembleResNet18;
```

经过训练的网络将作为`DAGNetwork`对象返回。

### 3. 图像分类

要使用网络对图像进行分类，请执行以下步骤：

```matlab
img = imresize(imread('peppers.png'), [224 224]);
predictedLabels = classify(net, img);
```

## 注意事项

- 确保已安装MATLAB R2018b或更高版本。
- 确保已安装深度学习工具箱。
- 图像输入大小必须为224×224×3。

通过以上步骤，您可以轻松地将ResNet-18应用于图像分类任务。

## 下载链接

[MATLAB神经网络工具箱代码导出-ResNet18](https://pan.quark.cn/s/3bb55d387635)