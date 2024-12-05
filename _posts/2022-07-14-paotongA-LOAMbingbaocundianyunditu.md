---
layout: post
title: "跑通A-LOAM并保存点云地图"
date:   2024-07-11
tags: [bash,LOAM,aloam,pcd,点云]
comments: true
author: admin
---
# 跑通A-LOAM并保存点云地图

本文旨在帮助读者迅速跑通3D激光SLAM算法A-LOAM，并保存点云地图。A-LOAM是一个基于激光雷达的SLAM算法，适用于自动驾驶、机器人导航等领域。通过本文的指导，您将能够安装A-LOAM、运行数据包、保存点云地图，并查看生成的点云地图。

## 一、A-LOAM安装

A-LOAM需要用到ceres库与pcl库，请确保已完成安装。

1. 创建工作空间：
   ```bash
   mkdir -p ~/aloam_ws/src
   cd ~/aloam_ws/src
   catkin_init_workspace
   ```

2. 克隆A-LOAM源码：
   ```bash
   git clone https://github.com/HKUST-Aerial-Robotics/A-LOAM.git
   ```

3. 编译：
   ```bash
   cd ~/aloam_ws
   catkin_make
   source ~/aloam_ws/devel/setup.bash
   ```

## 二、A-LOAM跑数据包

1. 运行A-LOAM：
   ```bash
   roslaunch aloam_velodyne aloam_velodyne_VLP_16.launch
   ```

2. 运行rosbag：
   ```bash
   rosbag play xxx.bag
   ```

## 三、Turtlebot3跑A-LOAM（velodyne16）

1. 启动Turtlebot3：
   ```bash
   roslaunch turtlebot3_bringup turtlebot3_robot.launch
   ```

2. 启动键盘控制：
   ```bash
   roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
   ```

3. 启动激光雷达：
   ```bash
   roslaunch velodyne_points VLP16_points.launch
   ```

4. 启动A-LOAM：
   ```bash
   roslaunch aloam_velodyne aloam_velodyne_VLP_16.launch
   ```

## 四、数据包创建

1. 启动A-LOAM后，另起终端开始记录数据：
   ```bash
   rosbag record -o xxx.bag /velodyne_points /laser_cloud_surround
   ```

## 五、点云地图保存与查看

### 点云地图保存

1. 方法一：
   ```bash
   rosrun pcl_ros bag_to_pcd xxx.bag /laser_cloud_surround pcd
   ```

2. 方法二：
   ```bash
   mkdir pcd
   cd pcd
   rosrun pcl_ros pointcloud_to_pcd input:=/laser_cloud_surround
   ```

### 点云地图查看

1. 使用pcl_viewer查看：
   ```bash
   pcl_viewer xxx.pcd
   ```

2. 将pcd点云地图转为ply格式：
   ```bash
   pcl_pcd2ply xxx.pcd xxxxxxx.ply
   ```

通过以上步骤，您可以成功跑通A-LOAM并保存点云地图。希望本文对您有所帮助！

## 下载链接

[跑通A-LOAM并保存点云地图](https://pan.quark.cn/s/c760ab2d714f)