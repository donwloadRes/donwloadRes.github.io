---
layout: post
title: "ArcGIS Pro二次开发：GeoProcessing工具和自定义工具的调用"
date:   2024-05-23
tags: [工具,自定义,二次开发,调用,ArcGIS]
comments: true
author: admin
---
# ArcGIS Pro二次开发：GeoProcessing工具和自定义工具的调用

本资源文件详细介绍了如何在ArcGIS Pro中进行二次开发，特别是如何调用系统自带的GeoProcessing工具以及自定义工具箱。通过本资源，您将学习到如何使用C#代码在ArcGIS Pro中实现这些功能。

## 主要内容

### 1. 调用GeoProcessing工具

- **缓冲区工具示例**：通过代码示例展示了如何使用`Geoprocessing.MakeValueArray()`方法生成工具所需的参数，并使用`Geoprocessing.ExecuteToolAsync()`方法执行缓冲区工具。
- **参数设置**：详细解释了如何按照顺序填写工具参数，并在参数为空值或采用默认值时使用`null`代替。

### 2. 调用自定义工具箱

- **自定义工具示例**：以自定义工具“ZH-消除重复要素”为例，展示了如何在`ExecuteToolAsync()`方法中输入完整的工具路径来调用自定义工具。
- **工具路径设置**：强调了在调用自定义工具时，需要输入工具的完整路径，并注意工具名与目录中显示的标注名的区别。

### 3. 工程文件分享

- **工程文件链接**：提供了工程文件的下载链接，方便用户自行下载并学习。

通过本资源文件，您将能够掌握在ArcGIS Pro中进行二次开发的基本技能，特别是如何调用和使用GeoProcessing工具及自定义工具箱。

## 下载链接

[ArcGISPro二次开发GeoProcessing工具和自定义工具的调用](https://pan.quark.cn/s/9a2df6cdd5aa)