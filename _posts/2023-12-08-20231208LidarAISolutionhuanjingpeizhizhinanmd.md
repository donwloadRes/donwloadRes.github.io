---
layout: post
title: "Lidar AI Solution 环境配置指南"
date:   2020-08-10
tags: [Lidar,AI,Solution,TensorRT,bash]
comments: true
author: admin
---
# Lidar AI Solution 环境配置指南

本文档旨在为 Lidar AI Solution 项目的环境配置提供详细的步骤和指导。通过本指南，您将能够顺利配置项目所需的环境，并开始使用 Lidar AI Solution 进行相关开发和研究。

## 项目概述

Lidar AI Solution 项目为自动驾驶中的 3D-Lidar 技术提供了一个高性能的解决方案。该项目在加速 sparse convolution、CenterPoint、BEVFusion 等方面表现出色，适用于多种自动驾驶场景。

## 环境配置步骤

### 1. 系统要求

- 操作系统：Ubuntu 20.04
- 显卡：RTX 3060
- 显卡驱动：510.108.03
- CUDA：11.6
- cuDNN：8.4.0
- TensorRT：8.4.1

### 2. 项目拉取

确保按照以下步骤完整拉取项目：

```bash
sudo apt-get install git-lfs
git clone --recursive https://github.com/NVIDIA-AI-IOT/Lidar_AI_Solution
cd Lidar_AI_Solution
```

**注意**：完整拉取项目非常重要，后续的问题基本上都是因为没有完整拉取整个项目所导致的。

### 3. 环境配置

#### 3.1 CUDA-BEVFusion

1. **下载模型和数据**

   从指定链接下载模型和数据到 `CUDA-BEVFusion` 文件夹，并解压。

2. **配置环境**

   修改 `environment.sh` 文件，设置 TensorRT、CUDA、CUDNN 的路径。

3. **编译运行**

   执行以下命令进行编译和运行：

   ```bash
   bash tool/build_trt_engine.sh
   bash tool/run.sh
   ```

#### 3.2 CUDA-CenterPoint

1. **模型和数据**

   使用 nuScenes Dataset 中的激光雷达数据，onnx 模型可以通过给定的脚本从 checkpoint 中导出。

2. **前置条件**

   确保安装了 CUDA、TensorRT、libspconv 库。

3. **编译运行**

   修改 `CMakeLists.txt` 文件，设置 TensorRT 和 CUDA 的路径，然后执行以下命令：

   ```bash
   bash tool/build_trt.sh
   mkdir -p build && cd build
   cmake .. && make -j
   ./centerpoint /data/test/ --verbose
   ```

#### 3.3 CUDA-PointPillars

1. **模型和数据**

   使用 KITTI 数据集中的激光雷达数据，onnx 文件可以通过脚本从预训练模型中导出。

2. **前置条件**

   确保安装了 TensorRT、CUDA 以及 TensorRT 中的 PillarScatter layer 插件。

3. **编译运行**

   修改 `CMakeLists.txt` 文件，设置 TensorRT 的路径，然后执行以下命令：

   ```bash
   mkdir -p build && cd build
   cmake .. && make -j
   ```

## 常见问题

1. **问题1：/usr/bin/ld：cannot find -lspconv**

   解决办法：确保完整拉取整个项目。

2. **问题2：/libspconv.so：file format not recognized**

   解决办法：确保完整拉取整个项目。

## 结语

通过以上步骤，您应该能够成功配置 Lidar AI Solution 项目的环境，并开始进行相关开发和研究。如果在配置过程中遇到任何问题，请参考项目文档或相关社区寻求帮助。

## 下载链接

[LidarAISolution环境配置指南](https://pan.quark.cn/s/2aba2df4cd40)