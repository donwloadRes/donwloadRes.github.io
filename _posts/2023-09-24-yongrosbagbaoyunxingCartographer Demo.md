---
layout: post
title: "用rosbag包运行Cartographer Demo"
date:   2021-03-31
tags: [Cartographer,rosbag,Demo,ROS,bash]
comments: true
author: admin
---
# 用rosbag包运行Cartographer Demo

## 简介
本资源文件提供了运行Cartographer Demo所需的rosbag包。通过使用这些rosbag包，用户可以在已安装Cartographer和Cartographer ROS的情况下，运行不同场景的Demo，包括Deutsches Museum、纯定位、静态路标、Revo LDS、PR2和Taurob Tracker。每个例子涉及不同的激光数据和参数配置，详细步骤如文所述。

## 使用方法
1. **前提条件**：确保已安装Cartographer和Cartographer ROS。
2. **重定位ROS环境**：部分运行前可能需要重定位ROS环境。
   ```bash
   source $HOME/catkin_ws/devel/setup.bash
   ```
   如果你的shell是zsh，则用zsh替代bash。
3. **下载和运行2d安装包**：
   - 下载离线包：
     ```bash
     wget -P ~/Downloads https://storage.googleapis.com/cartographer-public-data/bags/backpack_2d/cartographer_paper_deutsches_museum.bag
     ```
   - 运行Demo：
     ```bash
     roslaunch cartographer_ros demo_backpack_2d.launch bag_filename:=$HOME/Downloads/cartographer_paper_deutsches_museum.bag
     ```

## 注意事项
- 每个Demo涉及不同的激光数据和参数配置，请根据具体需求选择合适的rosbag包。
- 运行前请确保ROS环境已正确配置。

## 参考资料
- 详细步骤和更多信息请参考[CSDN博客文章](https://blog.csdn.net/windxf/article/details/104360370)。

## 下载链接

[用rosbag包运行CartographerDemo](https://pan.quark.cn/s/2d4124b0574f)