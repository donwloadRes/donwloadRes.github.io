---
layout: post
title: "OpenMVS详细安装教程Ubuntu 1804"
date:   2022-02-06
tags: [OpenMVS,安装,VCGLib,版本,源码]
comments: true
author: admin
---
# OpenMVS详细安装教程(Ubuntu 18.04)

本资源文件提供了在Ubuntu 18.04系统上安装OpenMVS的详细步骤。OpenMVS是一个用于多视角立体重建的开源库，能够从多个图像中创建高质量的三维模型。

## 安装步骤

### 1. 安装第三方库

在安装OpenMVS之前，需要先安装一些必要的第三方库，包括Eigen3、Boost、OpenCV、CGAL和VCGLib。

#### 1.1 安装Eigen3
建议使用Eigen3.4及以上版本，可以通过源码安装或通过Git下载。

#### 1.2 安装Boost
安装Boost 1.56版本及以上。

#### 1.3 安装OpenCV
安装OpenCV 2.4或更高版本。

#### 1.4 安装CGAL
安装CGAL库。

#### 1.5 安装VCGLib
通过Git下载VCGLib源码。

### 2. 安装OpenMVS

#### 2.1 下载OpenMVS源码
通过Git下载OpenMVS源码。

#### 2.2 编译和安装OpenMVS
使用CMake进行配置，并使用make命令进行编译和安装。

### 3. 测试OpenMVS

安装完成后，可以通过提供的测试数据集进行测试，验证OpenMVS的稠密重建、曲面重建、网格优化和纹理贴图功能。

## 常见问题及解决方案

在安装过程中可能会遇到一些问题，如VCGLib版本不兼容等。文章中提供了详细的解决方案，包括回退VCGLib版本等。

## 总结

本文详细介绍了在Ubuntu 18.04系统上安装OpenMVS的步骤，并提供了可能遇到的问题及解决方案。希望这份教程能够帮助你顺利完成OpenMVS的安装和配置。

## 下载链接

[OpenMVS详细安装教程Ubuntu18.04](https://pan.quark.cn/s/85f168aa6a1e)