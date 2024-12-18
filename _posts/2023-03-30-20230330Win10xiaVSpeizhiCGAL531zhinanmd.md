---
layout: post
title: "Win10下VS配置CGAL531指南"
date:   2021-10-03
tags: [CGAL,5.3,VS,安装,测试代码]
comments: true
author: admin
---
# Win10下VS配置CGAL-5.3.1指南

本资源文件提供了在Windows 10系统下，使用Visual Studio（VS）配置CGAL-5.3.1的详细步骤，包括下载、安装以及VS属性表配置，并附带测试代码。

## 内容概述

1. **CGAL概述**  
   CGAL（计算几何算法库）是一个C++算法库，提供了高效和可靠的几何算法。CGAL提供了许多数据结构和算法，如三角剖分、Voronoi图、多边形、单元复合体和多面体、曲线排列、网格生成、几何处理、凸包算法等。

2. **从源文档（Source Archive）中安装CGAL**  
   详细介绍了如何从源文档中下载并安装CGAL-5.3.1，包括CGAL、GMP和MPRF的安装步骤。

3. **VS属性表配置**  
   提供了在Visual Studio中配置CGAL的详细步骤，包括包含目录、库目录和附加依赖项的设置。

4. **测试代码**  
   附带了一个简单的测试代码，用于验证CGAL的安装和配置是否成功。

## 使用说明

1. **下载CGAL-5.3.1**  
   从CGAL官方网站下载CGAL-5.3.1的源代码压缩包，并解压缩到指定目录。

2. **安装GMP和MPRF**  
   下载并安装GMP和MPRF库，并将辅助文件夹拷贝到CGAL-5.3.1的解压目录下。

3. **安装Boost**  
   下载并安装Boost库，并设置环境变量。

4. **VS属性表配置**  
   在Visual Studio中创建新的项目属性表，并添加包含目录、库目录和附加依赖项。

5. **测试代码**  
   运行附带的测试代码，验证CGAL的安装和配置是否成功。

## 注意事项

- 确保所有依赖库（如Boost、GMP、MPRF）已正确安装并配置。
- 在配置VS属性表时，路径需根据实际安装路径进行调整。
- 测试代码仅供参考，可根据实际需求进行修改和扩展。

通过本指南，您将能够在Windows 10系统下，使用Visual Studio成功配置并使用CGAL-5.3.1进行开发。

## 下载链接

[Win10下VS配置CGAL-5.3.1指南](https://pan.quark.cn/s/c760e4408f6b)