---
layout: post
title: "Fastliolocalization完整跑通记录"
date:   2024-01-09
tags: [文档,源码,Fastlio,localization,跑通]
comments: true
author: admin
---
# Fastlio_localization完整跑通记录

本文档详细记录了Fastlio_localization的完整跑通过程，包括源码获取、编译、地图制作、运行及运行视频、脚本修改、结果保存等步骤。本文档适用于跑通官方数据集以及Apollo数据集。

## 目录
1. 源码获取
2. 数据集获取
3. 环境配置
4. 源码编译
5. 地图制作
6. 基于数据集的脚本参数修改
7. 源码运行
8. 结果保存

### 1. 源码获取
- 直接在GitHub上下载源码，地址为：https://github.com/HViktorTsoi/FAST_LIO_LOCALIZATION
- 或在Linux终端运行以下命令进行克隆：
  ```bash
  git clone https://github.com/HViktorTsoi/FAST_LIO_LOCALIZATION
  ```

### 2. 数据集获取
- 官方数据集和Apollo数据集的获取方式详见文档。

### 3. 环境配置
- 环境配置要求Python 2.7版本、PCL库（推荐PCL 1.7.2）、rosnumpy、open3d。
- 注意：所有依赖库需在Python 2.7环境下安装。

### 4. 源码编译
- 在工作空间下使用`catkin_make`进行编译。
- 常见问题及解决方法详见文档。

### 5. 地图制作
- 使用LIO-SAM提取每帧特征点制作地图。
- 地图效果展示详见文档。

### 6. 基于数据集的脚本参数修改
- 根据数据集特性修改脚本参数，如MAP_VOXEL_SIZE、SCAN_VOXEL_SIZE等。

### 7. 源码运行
- 运行前先source环境，然后使用`roslaunch`命令启动。
- 运行结果展示详见文档。

### 8. 结果保存
- 修改`transform_fusion.py`脚本以保存定位结果。

## 总结
本文档详细记录了Fastlio_localization的完整跑通过程，适用于官方数据集和Apollo数据集。如有任何问题，欢迎在评论区留言讨论。

## 下载链接

[Fastlio_localization完整跑通记录分享](https://pan.quark.cn/s/48377cecd7ee)