---
layout: post
title: "ROSnoetic  MAVROS  PX41123  Gazebo 多机协同仿真"
date:   2022-07-02
tags: [仿真,多机,bash,ROS,PX4]
comments: true
author: admin
---
# ROS-noetic + MAVROS + PX4-1.12.3 + Gazebo 多机协同仿真

## 简介

本资源文件提供了一个完整的ROS-noetic + MAVROS + PX4-1.12.3 + Gazebo多机协同仿真环境。所有代码已经调试完毕，可以直接使用。默认使用者的Ubuntu系统已经安装了PX4-Autopilot。

## 使用方法

1. **Source工作空间**  
   首先，请在终端中执行以下命令，以source本工作空间：
   ```bash
   source ~/multi_uav_test202206/devel/setup.bash
   ```

2. **打开QGroundControl（QGC）**  
   如果没有安装QGC，请自行下载并安装。打开QGC以监控无人机的状态。

3. **启动仿真**  
   打开一个新的终端，输入以下命令以启动仿真：
   ```bash
   roslaunch px4 multi_uav_mavros_sitl.launch
   ```

4. **运行控制节点**  
   再打开一个新的终端，输入以下命令以运行控制节点：
   ```bash
   rosrun offboard offboard_node
   ```

5. **观察仿真结果**  
   成功启动后，您将看到三架无人机按照圆形轨迹进行位置控制运动。

## 注意事项

- 在运行仿真之前，请确保修改`multi_uav_mavros_sitl.launch`文件中的无人机节点数量、ID以及对应的仿真UDP号，确保它们各不相同。

## 其他说明

本资源文件旨在帮助用户快速搭建并运行多机协同仿真环境。如有任何问题或建议，欢迎反馈。

## 下载链接

[ROS-noeticMAVROSPX4-1.12.3Gazebo多机协同仿真](https://pan.quark.cn/s/6584f987ef31)