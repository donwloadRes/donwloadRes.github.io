---
layout: post
title: "OSGB转3D Tiles工具分享"
date:   2021-02-11
tags: [转换,OSGB,3D,Tiles,工具]
comments: true
author: admin
---
# OSGB转3D Tiles工具分享

## 简介
本资源文件提供了一个将OSGB（倾斜摄影数据）转换为3D Tiles格式的工具。该工具适用于需要将倾斜摄影数据转换为3D Tiles格式以便在Cesium等平台上加载和展示的用户。

## 工具特点
- **高效转换**：支持快速将大型OSGB数据转换为3D Tiles格式。
- **简单易用**：操作简便，无需复杂的配置即可完成转换。
- **支持大数据**：无任何限制，支持超过10GB的大场景数据转换。

## 使用方法
1. **下载工具**：从本仓库下载提供的转换工具。
2. **搭建编译环境**：
   - 安装Visual Studio 2015（update 3）或VC 2015 C++ build tools（update 3）。
   - 配置Rustup的代理（仅限中国用户）。
3. **安装Rust**：
   - 下载并安装Rustup-init.exe自动安装工具。
   - 配置依赖源的代理。
4. **执行转换命令**：
   - 在命令行中进入工具目录，执行转换命令。

## 示例命令
```
3dtile.exe -f osgb -i E:\Data\倾斜摄影\hgc -o E:\Data\倾斜摄影\hgc_test
```

## 注意事项
- 确保输入的OSGB数据路径和输出的3D Tiles数据路径正确。
- 转换过程中可能需要一定的计算资源，建议在高性能计算机上进行。

## 感谢
感谢以下资源的分享，为本工具的开发提供了宝贵的参考：
- Cesium社区
- GitHub上的3dtiles项目
- 其他相关博客和技术文档

## 联系我们
如有任何问题或建议，欢迎通过仓库的Issues功能联系我们。

## 下载链接

[OSGB转3DTiles工具分享](https://pan.quark.cn/s/4741fa52dcfb)