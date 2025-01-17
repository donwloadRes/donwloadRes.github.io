---
layout: post
title: "NTURGBD数据集介绍及骨架数据可视化"
date:   2022-07-26
tags: [数据,RGB,NTU,可视化,骨架]
comments: true
author: admin
---
# NTU_RGB+D数据集介绍及骨架数据可视化

## 简介
NTU_RGB+D数据集是一个用于动作识别的大规模数据集，包含了56880个动作样本。每个样本包括RGB视频、深度图序列、3D骨架数据和红外视频等。数据集由3个Microsoft Kinect v2相机同时捕获，提供了丰富的多模态数据。

## 数据集内容
- **RGB视频**：分辨率为1920×1080。
- **深度图序列**：分辨率为512×424。
- **红外视频**：分辨率为512×424。
- **3D骨架数据**：每帧包含25个身体关节的三维坐标。

## 数据集结构
数据集文件命名格式如下：
- **S**：设置号，共有17组设置。
- **C**：相机ID，共有3架相机。
- **P**：人物ID，共有40个人。
- **R**：同一个动作的表演次数。
- **A**：动作类别，共有60个。

示例文件名：`S010C001P019R001A010_skeleton`

## 骨架数据可视化
本资源文件提供了Python代码，用于可视化NTU_RGB+D数据集中的3D骨架数据。代码支持2D和3D两种可视化方式，帮助用户更好地理解和分析数据集中的动作样本。

## 使用方法
1. **下载数据集**：从官方地址下载NTU_RGB+D数据集。
2. **运行代码**：使用提供的Python代码读取并可视化骨架数据。
3. **调整参数**：根据需要调整代码中的参数，如帧数、关节连接等。

## 注意事项
- 数据集较大，下载和处理可能需要较长时间。
- 可视化代码需要安装必要的Python库，如`numpy`、`matplotlib`等。

## 参考资料
- NTU_RGB+D数据集论文：CVPR2016
- 数据集官方下载地址：Skeleton_Data_Only（BaiDuYun）

## 更新日志
- 2024-01-14：更新了数据集下载地址和代码示例。

## 联系我们
如有任何问题或建议，请通过CSDN博客联系作者。

## 下载链接

[NTU_RGBD数据集介绍及骨架数据可视化分享](https://pan.quark.cn/s/83d34460db0c)