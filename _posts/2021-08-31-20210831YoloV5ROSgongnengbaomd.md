---
layout: post
title: "YoloV5 ROS功能包"
date:   2020-10-28
tags: [conda,yolov5,ROS,bash,PyTorch]
comments: true
author: admin
---
# YoloV5 ROS功能包

## 简介

本资源文件提供了一个基于PyTorch-YOLOv5的ROS功能包，允许用户在ROS（机器人操作系统）环境中使用YOLOv5进行实时目标检测。该功能包已在Ubuntu 16.04和Ubuntu 18.04上进行了测试，适用于ROS kinetic和melodic版本。

## 功能特点

- **实时目标检测**：利用YOLOv5的高效检测算法，实现对实时视频流的目标检测。
- **易于集成**：可以直接集成到现有的ROS项目中，方便与其他ROS功能包进行协作。
- **支持GPU加速**：默认情况下支持GPU加速，提高检测速度。
- **自定义权重**：用户可以将自己训练的权重文件放入weights文件夹中，进行自定义检测。

## 安装步骤

### 1. 安装Anaconda

1. 下载对应的Anaconda安装包。
2. 执行脚本安装Anaconda：
   ```bash
   bash ~/Downloads/Anaconda3-2021.05-Linux-x86_64.sh
   ```

### 2. 安装PyTorch

1. 创建Python 3.6以上版本的conda环境：
   ```bash
   conda create -n mypytorch python=3.8
   ```
2. 激活创建好的conda环境：
   ```bash
   conda activate mypytorch
   ```
3. 在PyTorch官网上选择指定版本安装PyTorch：
   ```bash
   conda install pytorch torchvision torchaudio cpuonly -c pytorch
   ```

### 3. 安装Yolov5_ROS

1. 克隆Yolov5_ROS功能包到您的catkin工作空间的src目录中：
   ```bash
   cd /your/catkin_ws/src
   git clone https://github.com/qq44642754a/Yolov5_ros.git
   ```
2. 进入yolov5_ros/yolov5目录，并安装所需的Python依赖项：
   ```bash
   cd yolov5_ros/yolov5
   sudo pip install -r requirements.txt
   ```

## 基本用法

1. 确保将您训练好的权重文件放在weights文件夹中。默认情况下，`launch/yolo_v5.launch`文件使用`yolov5s.pt`权重文件。
2. 在launch文件中修改摄像头话题名称和是否使用CPU选项。
3. 运行yolov5 ROS节点：
   ```bash
   roslaunch yolov5_ros yolo_v5.launch
   ```

## 特殊说明

鉴于最近有很多人安装配置不好yolov5的环境，我这边配置好了一个名为yolov5的conda环境。您可以通过百度网盘下载并解压后放入`/anaconda3/envs/`文件夹下，然后运行以下指令添加到conda环境中：
```bash
conda config --add envs_dirs 下载好的yolov5文件夹的路径
```
最后通过指令`conda activate yolov5`来激活conda环境。

## 作者

- Zhitao Zheng (qq44642754@163.com)

## 开发环境

- Ubuntu 16.04 / 18.04
- ROS kinetic/melodic
- Python >= 3.6.0
- PyTorch >= 1.7

## 下载链接

[YoloV5ROS功能包分享](https://pan.quark.cn/s/74a429129145)