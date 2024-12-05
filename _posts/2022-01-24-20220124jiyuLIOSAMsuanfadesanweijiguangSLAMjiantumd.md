---
layout: post
title: "基于LIOSAM算法的三维激光SLAM建图"
date:   2021-01-24
tags: [LIO,SAM,算法,SLAM,建图]
comments: true
author: admin
---
# 基于LIO-SAM算法的三维激光SLAM建图

本资源文件提供了基于LIO-SAM算法的三维激光SLAM建图的实现和相关数据集。LIO-SAM是一种结合了激光雷达（LiDAR）和惯性测量单元（IMU）的实时定位与建图（SLAM）算法，具有高效性和鲁棒性。

## 内容概述

- **LIO-SAM算法实现**：提供了LIO-SAM算法的源代码，用户可以在自己的环境中进行编译和运行。
- **数据集**：包含用于测试LIO-SAM算法的数据集，用户可以使用这些数据集进行实验和验证。

## 使用说明

### 1. 环境配置

- **操作系统**：Ubuntu 18.04
- **ROS版本**：Melodic
- **依赖库**：
  - Ceres Solver 2.0.0
  - PCL 1.8.1
  - gtsam-4.0.0-alpha2 或 4.0.2

### 2. 安装步骤

1. 创建工作空间：
   ```bash
   mkdir -p ~/catkin_ws_liosam/src
   cd ~/catkin_ws_liosam/src
   ```

2. 下载源码并编译：
   ```bash
   git clone https://github.com/TixiaoShan/LIO-SAM.git
   cd ..
   catkin_make
   ```

3. 下载数据集：
   - 数据集文件位于`src/data`目录下，用户可以根据需要下载并放置在该目录中。

### 3. 运行LIO-SAM

1. 启动LIO-SAM：
   ```bash
   roslaunch lio_sam run.launch
   ```

2. 播放数据包：
   ```bash
   rosbag play ~/catkin_ws_liosam/src/data/casual_walk.bag
   ```

### 4. 保存建图结果

1. 修改配置文件：
   - 在`params.yaml`文件中设置`SavePCD`为`true`，并指定保存路径。

2. 设置超时时间：
   - 修改`/opt/ros/melodic/lib/python2.7/dist-packages/roslaunch/nodeprocess.py`文件中的`_TIMEOUT_SIGINT`值为100秒。

3. 保存结果：
   ```bash
   pcl_viewer GlobalMap.pcd
   pcl_viewer CornerMap.pcd
   pcl_viewer SurfMap.pcd
   pcl_viewer trajectory.pcd
   pcl_viewer transformations.pcd
   ```

## 参考文献

- LIO-SAM: Tixiao Shan, et al. "LIO-SAM: Tightly-coupled Lidar Inertial Odometry via Smoothing and Mapping." IROS 2020.

## 注意事项

- 在运行过程中，请确保所有依赖库已正确安装。
- 数据集文件较大，下载时请耐心等待。

通过本资源文件，用户可以快速上手LIO-SAM算法，并进行三维激光SLAM建图的实验和应用。

## 下载链接

[基于LIO-SAM算法的三维激光SLAM建图](https://pan.quark.cn/s/2ec3ed0ebed0)