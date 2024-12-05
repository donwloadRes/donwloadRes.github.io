---
layout: post
title: "zlib123dllx64 资源文件下载"
date:   2022-04-19
tags: [文件,zlib123dllx64,dll,下载,lib]
comments: true
author: admin
---
# zlib123dllx64 资源文件下载

## 描述

在进行TensorRT加速时，可能会遇到CMake编译失败的问题，提示缺少`zlibwapi.dll`。错误信息如下：

```
Could not locate zlibwapi.dll. Please make sure it is in your library path
```

为了解决这个问题，您需要将`lib`文件放到`C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.1\lib`目录下，并将`dll`文件放到`C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.1\bin`目录下。

本仓库提供的资源文件`zlib123dllx64`即为解决上述问题的所需文件。请根据您的系统架构选择合适的版本进行下载。

## 使用说明

1. **下载资源文件**：在本仓库中下载`zlib123dllx64`文件。
2. **放置文件**：
   - 将`lib`文件放到`C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.1\lib`目录下。
   - 将`dll`文件放到`C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.1\bin`目录下。
3. **验证**：重新运行CMake编译，确保问题已解决。

## 注意事项

- 请确保下载的`zlib123dllx64`文件与您的系统架构（64位）匹配。
- 如果您使用的是32位系统，请下载32位的ZLIB DLL。

通过以上步骤，您应该能够成功解决CMake编译过程中缺少`zlibwapi.dll`的问题。

## 下载链接

[zlib123dllx64资源文件下载](https://pan.quark.cn/s/733ac4017662)