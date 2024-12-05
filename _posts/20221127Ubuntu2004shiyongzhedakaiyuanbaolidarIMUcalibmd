---
layout: post
title: "Ubuntu 20.04 使用浙大开源包 lidar_IMU_calib"
date:   2024-02-01
tags: [标定,IMU,源码,calib,Lidar]
comments: true
author: admin
---
# Ubuntu 20.04 使用浙大开源包 lidar_IMU_calib

## 简介
本资源文件提供了在Ubuntu 20.04系统上使用浙大开源包lidar_IMU_calib进行Lidar和IMU标定的详细指南。该工具包允许用户在没有目标的情况下进行Lidar和IMU的标定，适用于多种类型的激光雷达。

## 主要内容
1. **编译源码**：详细介绍了如何在Ubuntu 20.04上编译lidar_IMU_calib工具包的源码。
2. **源码修改**：针对不同型号的激光雷达，提供了源码修改的方法，以适配特定的雷达型号。
3. **录制数据集**：指导用户如何录制标定所需的数据集，确保数据集的质量和完整性。
4. **标定运行**：介绍了两种运行标定过程的方法，并提供了可能遇到的问题及其解决方案。
5. **标定结果**：解释了标定结果的含义，帮助用户理解和应用标定数据。

## 使用步骤
1. **编译**：
   - 创建工作空间并初始化。
   - 下载源码并安装依赖。
   - 编译源码并设置环境变量。

2. **源码修改**：
   - 根据雷达型号修改源码，主要涉及`/include/utils/vlp_common.h`、`dataset_reader.h`和`/src/ui/calib_helper.cpp`文件。

3. **录制数据集**：
   - 在室内平面较多的地方录制数据集，确保Lidar和IMU在各个方向上充分旋转和移动。

4. **标定运行**：
   - 修改launch文件中的参数，设置录制的bag包地址和持续时间。
   - 运行标定过程，解决可能出现的错误。

5. **标定结果**：
   - 分析标定结果，理解Lidar在IMU坐标系下的平移和旋转矩阵。

## 注意事项
- 在编译过程中，注意PCL和Pangolin的版本兼容性问题。
- 录制数据集时，确保Lidar和IMU固定，避免在狭窄的小房间内录制。
- 运行标定时，根据实际情况调整launch文件中的参数。

通过本资源文件，用户可以顺利在Ubuntu 20.04系统上使用浙大开源包lidar_IMU_calib进行Lidar和IMU的标定，提升传感器数据的准确性和可靠性。

## 下载链接

[Ubuntu20.04使用浙大开源包lidar_IMU_calib](https://pan.quark.cn/s/47fb6e0fd4b0)