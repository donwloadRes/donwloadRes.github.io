---
layout: post
title: "KITTI数据集下载（百度云）"
date:   2022-06-03
tags: [object,KITTI,data,下载,解压]
comments: true
author: admin
---
# KITTI数据集下载（百度云）

## 简介
KITTI数据集是由德国卡尔斯鲁厄理工学院和丰田美国技术研究院联合创办的，是目前国际上最大的自动驾驶场景下的计算机视觉算法评测数据集。该数据集用于评测立体图像、光流、视觉测距、3D物体检测和3D跟踪等计算机视觉技术在车载环境下的性能。

## 数据集内容
KITTI数据集包含市区、乡村和高速公路等场景采集的真实图像数据，每张图像中最多达15辆车和30个行人，还有各种程度的遮挡与截断。数据集包括以下文件：
- data_object_calib
- data_object_image_2
- data_object_label_2
- data_object_velodyne
- data_object_velodyne
- devkit_object

## 下载方式
由于KITTI官网提供的链接国内无法下载，网络上的资源也大部分失效，因此我们将数据集重新上传到百度云，方便大家下载。

## 使用说明
1. 每个文件的内容被分成多个压缩包，主要是因为百度云对上传文件的大小有限制，另外压缩后的文件确实比原始文件小很多。
2. 对于不同内容的压缩包，只需要解压对应的xxx.zip文件。
3. 若出现解压后文件被损坏，可能是下载的时候数据被破坏了，或者使用的解压软件不对，建议使用Bandizip软件进行解压。

## 其他资源
我们还整理了三维目标检测相关内容，包括经典论文的分类、下载、代码和笔记，以及基于OpenPCDet框架的基线模型下载及性能评估。

## 注意事项
请确保下载过程中网络稳定，避免数据损坏。解压时建议使用Bandizip软件，以确保文件完整性。

## 下载链接

[KITTI数据集下载百度云](https://pan.quark.cn/s/a064bce859d1)