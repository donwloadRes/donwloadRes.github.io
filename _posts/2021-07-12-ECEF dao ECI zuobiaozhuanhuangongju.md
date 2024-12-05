---
layout: post
title: "ECEF 到 ECI 坐标转换工具"
date:   2020-09-15
tags: [ECEF,ECI,坐标,格式,矢量]
comments: true
author: admin
---
# ECEF 到 ECI 坐标转换工具

## 描述

本资源文件提供了一个 MATLAB 函数，用于将 WGS 84 (CTS ECEF) 坐标转换为 ECI (CIS Epoch J2000.0) 坐标。该函数已被矢量化以提高处理速度，并且与 STK 星历输出相比，坐标系之间转换的相关误差约为 1.2*10^-11 公里。

## 使用方法

要运行此函数，请在 MATLAB 提示符下键入以下命令：

```matlab
[r_ECI, v_ECI, a_ECI] = ECEFtoECI(JD, r_ECEF, v_ECEF, a_ECEF);
```

### 参数说明

- `JD`：儒略日期向量，格式为 `[1 x N]`。
- `r_ECEF`：ECEF 坐标中的位置向量，格式为 `[3 x N]`。
- `v_ECEF`：ECEF 坐标中的速度矢量，格式为 `[3 x N]`。
- `a_ECEF`：ECEF 坐标中的加速度矢量，格式为 `[3 x N]`。

### 输出

- `r_ECI`：ECI 坐标中的位置向量，格式为 `[3 x N]`。
- `v_ECI`：ECI 坐标中的速度矢量，格式为 `[3 x N]`。
- `a_ECI`：ECI 坐标中的加速度矢量，格式为 `[3 x N]`。

## 注意事项

- 该函数适用于处理任何矢量或矢量系列，能够高效地将它们从 ECEF 坐标系转换到 ECI 坐标系。
- 转换误差非常小，适用于高精度的坐标转换需求。

## 适用场景

该工具适用于需要将地球固定坐标系（ECEF）中的数据转换为地心惯性坐标系（ECI）的场景，例如卫星轨道计算、天体导航等领域。

## 下载链接

[ECEF到ECI坐标转换工具](https://pan.quark.cn/s/7ff77eb2492f)