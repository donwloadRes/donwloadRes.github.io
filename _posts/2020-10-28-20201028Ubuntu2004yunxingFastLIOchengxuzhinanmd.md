---
layout: post
title: "Ubuntu 2004运行FastLIO程序指南"
date:   2024-02-17
tags: [LIO,Livox,Fast,SDK,bash]
comments: true
author: admin
---
# Ubuntu 20.04运行Fast-LIO程序指南

本资源文件提供了在Ubuntu 20.04系统上运行Fast-LIO程序的详细步骤和相关配置说明。Fast-LIO（Fast LiDAR-Inertial Odometry）是一种计算效率高、鲁棒的里程计软件包，它利用紧密耦合的迭代扩展卡尔曼滤波器将激光雷达特征点与IMU数据融合，从而在快速运动、噪声或混乱的环境中实现鲁棒导航。

## 内容概述

本资源文件包含以下主要内容：

1. **Livox-sdk安装**：详细介绍了如何安装Livox-SDK，并配置相关环境变量。
2. **Livox_ros_driver安装**：指导用户如何安装Livox ROS驱动，并进行编译。
3. **FAST_LIO安装**：提供了FAST_LIO的安装步骤，包括下载、编译和配置。
4. **Velodyne Rosbag TEST**：介绍了如何使用Velodyne雷达进行测试，并确保topic配置正确。

## 使用步骤

### 1. Livox-sdk安装

```bash
git clone https://github.com/Livox-SDK/Livox-SDK.git
cd Livox-SDK
cd build && cmake ..
make
sudo make install
```

### 2. Livox_ros_driver安装

```bash
git clone https://github.com/Livox-SDK/livox_ros_driver.git ws_livox/src
cd ws_livox/
catkin_make
source devel/setup.sh
```

### 3. FAST_LIO安装

```bash
# 下载FAST_LIO源码并移动到ws_livox/src下
cd ws_livox/
source devel/setup.bash
catkin_make
```

### 4. Velodyne Rosbag TEST

```bash
roslaunch fast_lio mapping_velodyne.launch
rosbag play YOUR_DOWNLOADED_BAG
```

## 注意事项

- 在启动`mapping_velodyne.launch`文件之前，务必确认Velodyne雷达配置文件中的topic与bag文件中数据的topic一致。
- 确保所有依赖库已正确安装，包括ROS、PCL、Eigen等。

通过以上步骤，您可以在Ubuntu 20.04系统上成功运行Fast-LIO程序，并进行相关测试和开发。

## 下载链接

[Ubuntu20.04运行Fast-LIO程序指南分享](https://pan.quark.cn/s/91972cd9796d)