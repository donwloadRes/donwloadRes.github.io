---
layout: post
title: "S3DIS场景点云数据集"
date:   2020-03-29
tags: [数据,S3DIS,场景,包含,维度]
comments: true
author: admin
---
# S3DIS场景点云数据集

## 简介
S3DIS（Stanford Large-Scale 3D Indoor Spaces Dataset）是一个大规模的三维室内空间数据集，广泛应用于点云分类、分割等领域。该数据集包含了多个室内环境的数据，如办公室、会议室等，提供了详细的点云数据和语义标签。

## 数据集结构
S3DIS数据集包含6个Area，每个Area包含了不同的场景（如会议室、走廊等）。每个场景的点云数据以txt文件格式存储，包含了点的xyz坐标和rgb颜色信息。此外，每个场景还包含一个Annotations文件夹，其中包含了不同类别的点位置及其RGB颜色。

## 数据格式
- **Stanford3dDataset_v1.2_Aligned_Version**: 完整的场景数据集，每个点包含6个维度（x, y, z, r, g, b）。
- **indoor3d_sem_seg_hdf5_data**: 将场景切割成1m x 1m的block，每个block包含4096个点，每个点有9个维度（前6个维度和上面的一样，后3个维度表示相对于所在大场景的位置）。

## 使用方法
1. 下载数据集并解压缩。
2. 根据需要选择合适的场景和数据格式进行处理。
3. 使用点云处理工具（如PointNet、PointNet++等）进行数据分析和模型训练。

## 注意事项
- 数据集较大，下载和处理时需要足够的存储空间和计算资源。
- 数据集的标注信息较为详细，适合用于语义分割和实例分割任务。

## 参考资料
- 更多关于S3DIS数据集的详细信息和使用方法，请参考相关文献和官方文档。

## 下载链接

[S3DIS场景点云数据集分享](https://pan.quark.cn/s/07970ef4c6b8)