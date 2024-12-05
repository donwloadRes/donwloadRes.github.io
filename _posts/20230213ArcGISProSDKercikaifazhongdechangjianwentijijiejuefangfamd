---
layout: post
title: "ArcGIS Pro SDK二次开发中的常见问题及解决方法"
date:   2022-09-16
tags: [Pro,SDK,ArcGIS,二次开发,版本]
comments: true
author: admin
---
# ArcGIS Pro SDK二次开发中的常见问题及解决方法

本文总结了在ArcGIS Pro SDK二次开发过程中常见的问题及其解决方法。这些问题涵盖了从环境配置到具体开发过程中遇到的各类技术难题，旨在帮助开发者更顺利地进行ArcGIS Pro的二次开发。

## 一、在VS2022中进行调试弹出错误

在Visual Studio 2022中进行调试时，可能会遇到弹出错误提示框并导致死机的情况。这通常是由于破解文件AfCore.dll的问题引起的。解决方法是下载一个可用的破解版本，并将其替换到Pro安装目录的【bin】文件夹下。

## 二、ArcGIS Pro SDK版本和当前Pro版本不一致

在添加SDK项目时，可能会出现SDK版本与当前使用的Pro版本不一致的错误。目前Pro的破解版只停留在3.0.x，因此SDK版本也应选择3.0。如果SDK自动更新导致版本不一致，可以在VS2022中关闭自动更新，并重新安装3.0版本的SDK。

## 三、AddIn项目中的图标图片无法正常显示

在AddIn项目中，替换Button等控件的默认图标时，可能会发现图标并未变化。这是因为图片属性中的【生成操作】默认为【无】，将其修改为【内容】即可解决问题。

## 四、SHP图层的自定义右键菜单栏无效

在图层的右键菜单栏中添加自定义按钮时，如果图层数据是SHP格式，自定义按钮可能不会显示。这是因为SHP图层在SDK中被视为unregisteredLayer。解决方法是将所属位置改为【esri_mapping_unregisteredLayerContextMenu】。

## 五、GeometryEngine用法详解

GeometryEngine是ArcGIS Pro SDK中的关键组件，提供了一系列处理几何图形的方法和算法。本文汇总了在开发中可能会用到的功能，方便开发者查询和使用。

## 六、面积平差工具

在数据处理过程中，可能会需要进行面积平差。本文介绍了一个面积平差工具的使用方法，帮助开发者更高效地处理数据。

## 七、ArcGIS Pro中的多线程

ArcGIS Pro采用多线程架构，可以有效发挥多核CPU的优势。本文介绍了在ArcGIS Pro二次开发中如何处理多线程，以提升工具性能。

通过以上问题的总结和解决方法的介绍，希望能帮助ArcGIS Pro SDK的开发者更顺利地进行二次开发工作。

## 下载链接

[ArcGISProSDK二次开发中的常见问题及解决方法](https://pan.quark.cn/s/82b293657a0e)