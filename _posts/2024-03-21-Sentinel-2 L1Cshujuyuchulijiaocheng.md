---
layout: post
title: "Sentinel-2 L1C数据预处理教程"
date:   2021-11-04
tags: [ENVI,波段,Sen2Cor,采样,教程]
comments: true
author: admin
---
# Sentinel-2 L1C数据预处理教程

本资源文件提供了详细的Sentinel-2哨兵二号L1C数据预处理教程，涵盖了使用Sen2Cor进行大气校正、SNAP进行重采样以及ENVI进行波段组合的步骤。

## 内容概述

1. **Sen2Cor大气校正**
   - 单文件处理
   - 批量处理

2. **SNAP重采样**
   - 打开影像
   - 重采样设置

3. **ENVI波段组合**
   - 加载波段
   - 波段组合

## 使用说明

### 1. Sen2Cor大气校正

#### 单文件处理
- 使用命令提示符（CMD）切换到Sen2Cor目录。
- 输入命令`L2A_Process.bat + 影像路径`进行处理。

#### 批量处理
- 使用命令提示符（CMD）切换到Sen2Cor目录。
- 输入批量处理命令`for /D %s in (影像路径*) do L2A_process %s`。

### 2. SNAP重采样

#### 打开影像
- 在SNAP中打开L2A数据文件夹中的`MTD_MSIL2A.xml`文件。

#### 重采样
- 使用`Optical > Geometric > S2 Resampling Processor`工具。
- 设置导出格式为ENVI，修改导出路径和分辨率（如10m），点击Run。

### 3. ENVI波段组合

#### 加载波段
- 将重采样完成后的`.img`波段文件拖入ENVI打开。

#### 波段组合
- 使用`Build Layer Stack`工具（ENVI 5.6以上版本）或`Layer Stacking`工具（ENVI 5.3版本）。
- 按顺序导入波段，选择坐标系，输出波段组合。

## 总结

本教程详细介绍了Sentinel-2数据的预处理流程，适用于从官网下载的L2A级数据。通过本教程，您可以掌握如何使用Sen2Cor进行大气校正，使用SNAP进行重采样，以及使用ENVI进行波段组合，以便于后期的定量分析。

## 下载链接

[Sentinel-2L1C数据预处理教程](https://pan.quark.cn/s/60467d107762)