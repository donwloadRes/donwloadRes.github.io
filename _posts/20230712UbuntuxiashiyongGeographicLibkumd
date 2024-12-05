---
layout: post
title: "Ubuntu下使用GeographicLib库"
date:   2021-07-15
tags: [GeographicLib,bash,lib,libGeographic,Ubuntu]
comments: true
author: admin
---
# Ubuntu下使用GeographicLib库

## 简介

本资源文件提供了在Ubuntu系统下使用GeographicLib库的详细步骤和指南。GeographicLib是一个用于地理计算的C++库，支持地理坐标、UTM、UPS、MGRS、地心坐标和局部笛卡尔坐标之间的转换，以及重力和地磁场的计算。

## 安装步骤

1. **下载GeographicLib库**  
   这里下载的是1.48版本，也可以根据需要下载其他版本。

2. **解压**  
   ```bash
   tar xfpz GeographicLib-1.48.tar.gz
   ```

3. **进入文件目录**  
   ```bash
   cd GeographicLib-1.49
   ```

4. **创建build文件夹并进入**  
   ```bash
   mkdir build
   cd build
   ```

5. **配置**  
   使用库中自带文件进行配置：
   ```bash
   ../configure
   ```

6. **编译和安装**  
   ```bash
   make
   make install
   ```

7. **在项目文件的CMakeLists.txt中加入依赖**  
   在CMakeLists.txt中加入GeographicLib需要的依赖：
   ```cmake
   LIST(APPEND LINK_LIBS $[OpenCV_LIBS] #$ENV[HOME]/ScaViSLAM/svslocal/lib/libGeographic.so #$[Geographic_LIBS]/usr/local/lib/libGeographic.a /usr/local/lib/libGeographic.so.17.1.1 /usr/local/lib/libGeographic.so.17 /usr/local/lib/libGeographic.so)
   ```

8. **解决egm2008问题**  
   如果在运行时遇到“找不到egm2008”的问题，需要下载egm2008库：
   ```bash
   geographiclib-get-gravity all # to install egm84, egm96, egm2008, wgs84
   ```

## 总结

通过上述步骤，您可以在Ubuntu系统下成功安装和使用GeographicLib库。该库提供了丰富的地理计算功能，适用于各种地理信息处理项目。

## 下载链接

[Ubuntu下使用GeographicLib库分享](https://pan.quark.cn/s/be88bd5877f3)