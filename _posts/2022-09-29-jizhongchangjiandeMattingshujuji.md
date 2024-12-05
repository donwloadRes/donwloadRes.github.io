---
layout: post
title: "几种常见的Matting数据集"
date:   2024-08-29
tags: [Matting,数据,图像,PPM,636]
comments: true
author: admin
---
# 几种常见的Matting数据集

本文整理了多种Matting数据集，包括alphamatting、PPM-100、Matting_Human_Half、RealWorldPortrait-636、PhotoMatte85、DVM、AIM-500等。所有数据集已经打包放在百度云盘，大家可以自由下载。

## 数据集列表

1. **alphamatting**  
   2009年的一片CVPR提出的数据集，数据量较少，可作为一个toy dataset玩玩。

2. **PPM-100**  
   PPM是一种具有以下特征的人像抠图数据集：
   - 精细注释：所有图像都经过仔细标记和检查
   - 自然背景：所有图像都使用原始背景，无需替换
   - 丰富多样性：图像涵盖全身/半身和各种姿势
   - 高分辨率：图像的分辨率在1080p到4k之间

3. **Matting_Human_Half**  
   该数据集是人体半身图像，包含34427对图像-matting图，是目前已知最大的人像Matting数据集。

4. **RealWorldPortrait-636**  
   Mask Guided Matting via Progressive Refinement Network (CVPR 2021)中提出的一个数据集，包含636张人像及其对应的标注（alpha, detail map, segmask）。

5. **PhotoMatte85**  
   这个数据集只有85张高质量的原图及蒙版，可用于测试，另外还有13K的训练集，作者没有公开。

6. **DVM**  
   包含了高质量的视频前景和背景，可通过视频抽帧的方式得到图片数据集，具体参考：https://github.com/nowsyn/DVM。

7. **AIM-500**  
   该数据集包含500个不同类型的自然图像及其对应标注的alpha图。

8. **Matting (hair&faces)-demo**  
   20张包含人体上半部分的数据集，是一个Demo数据集，原始大小的数据为商用。

## 下载方式

所有数据集已经打包放在百度云盘，大家可以自由下载。提取码为5apj。

## 注意事项

请注意，这些数据集是由计算机模拟的颜色，不同设备上显示也有所区别，实际生产中请参阅最新出版的实物色卡确认。

## 下载链接

[几种常见的Matting数据集](https://pan.quark.cn/s/e3922083a3e0)