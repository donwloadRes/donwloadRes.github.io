---
layout: post
title: "RK系列升级内核中的RKNPU驱动"
date:   2020-08-16
tags: [RKNPU,升级,内核,0.8,rknpu]
comments: true
author: admin
---
# RK系列升级内核中的RKNPU驱动

## 简介

本资源文件提供了RK系列芯片（如RK3588和RK356X）内核中RKNPU驱动的升级方法。由于当前内核中的RKNPU版本过低，导致C语言的推理无法进行，因此需要进行驱动方面的升级。本教程详细介绍了如何将RKNPU驱动从0.8.2升级到0.8.8，以解决C接口无法调用的问题。

## 升级步骤

1. **解压驱动文件**：
   - 解压 `rk3588_kernel_drivers_rknpu_0.8.8.tar.gz` 文件，并将其内容替换到 `SDK/kernel/drivers` 目录中。

2. **重新编译内核**：
   - 在SDK根目录下执行 `/build.sh kernel` 命令，以重新编译内核。

3. **烧录内核镜像**：
   - 编译完成后，将生成的 `boot.img` 文件（位于 `SDK/rockdev/` 目录）烧录到设备的boot分区。

4. **验证升级**：
   - 重启设备后，执行 `dmesg | grep rknpu` 命令，查看RKNPU版本是否已成功升级至0.8.8。

## 测试结果

升级成功后，系统日志中将显示如下信息：
```
[ 4.482983] RKNPU fdab0000 npu: RKNPU: rknpu iommu is enabled using iommu mode
[ 4.483810] [drm] Initialized rknpu 0.8.8 20230428 for fdab0000 npu on minor 1
[ 4.486180] debugfs: Directory 'fdab0000 npu-rknpu' with parent 'vdd_npu_s0' already present
```

## 注意事项

- 升级前请确保备份原有驱动文件，以防升级失败。
- 升级过程中请确保设备电源稳定，避免因断电导致升级失败。

## 适用平台

本教程适用于RK3588和RK356X系列芯片。

## 下载链接

[RK系列升级内核中的RKNPU驱动](https://pan.quark.cn/s/4b5a472a4093)