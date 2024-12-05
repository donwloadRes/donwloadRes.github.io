---
layout: post
title: "在ROS下编译ORBSLAM2遇到错误Pangolin依赖Eigen3未找到的解决方案"
date:   2021-11-14
tags: [Pangolin,Eigen3,ORB,SLAM2,could]
comments: true
author: admin
---
# 在ROS下编译ORB_SLAM2遇到错误：Pangolin依赖Eigen3未找到的解决方案

## 简介

本资源文件提供了一个解决方案，用于解决在ROS环境下编译ORB_SLAM2时遇到的错误：`Pangolin could not be found because dependency Eigen3 could not be found`。该错误通常是由于Pangolin库的版本过高或Eigen3库未正确安装导致的。

## 问题描述

在ROS下编译ORB_SLAM2时，可能会遇到以下错误信息：

```
Pangolin could not be found because dependency Eigen3 could not be found
```

该错误通常是由于Pangolin库的版本过高或Eigen3库未正确安装导致的。

## 解决方案

### 1. 检查Eigen3库

首先，确保Eigen3库已正确安装。可以通过以下命令检查：

```bash
sudo apt-get install libeigen3-dev
```

### 2. 降低Pangolin版本

如果Eigen3库已安装但问题仍然存在，可能是因为Pangolin库的版本过高。建议将Pangolin库降级到0.5版本。

#### 步骤如下：

1. 删除当前的Pangolin库：

   ```bash
   sudo rm -rf /usr/local/include/pangolin /usr/local/lib/libpangolin*
   ```

2. 下载并安装Pangolin 0.5版本：

   ```bash
   git clone https://github.com/stevenlovegrove/Pangolin.git
   cd Pangolin
   git checkout v0.5
   mkdir build
   cd build
   cmake ..
   make -j4
   sudo make install
   ```

3. 重新编译ORB_SLAM2：

   ```bash
   cd ORB_SLAM2
   ./build.sh
   ./build_ros.sh
   ```

### 3. 验证安装

完成上述步骤后，重新编译ORB_SLAM2，检查是否解决了`Pangolin could not be found because dependency Eigen3 could not be found`的问题。

## 总结

通过降低Pangolin库的版本到0.5，可以有效解决在ROS下编译ORB_SLAM2时遇到的`Pangolin could not be found because dependency Eigen3 could not be found`错误。希望本解决方案能帮助你顺利完成ORB_SLAM2的编译。

## 下载链接

[在ROS下编译ORB_SLAM2遇到错误Pangolin依赖Eigen3未找到的解决方案分享](https://pan.quark.cn/s/7ea7a4b7f586)