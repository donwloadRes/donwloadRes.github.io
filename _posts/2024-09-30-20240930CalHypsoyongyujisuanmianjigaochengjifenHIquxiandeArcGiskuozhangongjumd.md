---
layout: post
title: "CalHypso用于计算面积高程积分HI曲线的ArcGis扩展工具"
date:   2020-09-18
tags: [高程,CalHypso,积分,曲线,计算]
comments: true
author: admin
---
# CalHypso——用于计算面积高程积分（HI）曲线的ArcGis扩展工具

## 简介
CalHypso是一款由J.V. Pérez-Peña教授开发的ArcGIS扩展工具，专门用于计算面积高程积分（HI）曲线。该工具自2009年开发以来，已被广泛应用于构造地貌的研究中，极大地节省了研究人员绘制面积高程积分曲线的时间。

## 功能特点
- **高效计算**：能够快速计算面积高程积分曲线，提高研究效率。
- **易于使用**：安装简单，操作界面友好，适合各类研究人员使用。
- **广泛应用**：适用于构造地貌、水文地质等多个领域的研究。

## 使用方法
1. **下载与安装**：
   - 下载CalHypso插件文件。
   - 双击解压后的文件夹中的`CalHypsoAddIn.esriAddIn`文件，安装插件。

2. **启动与配置**：
   - 打开ArcMap，点击“自定义”→“自定义模式”。
   - 在“类别”中找到“Geomorphic Indexes”，将“Hypsometric curve”命令拖动到任意工具条上。

3. **数据加载与计算**：
   - 选择DEM数据和流域面要素。
   - 点击“Load data”按钮，即可计算面积高程积分曲线。
   - 点击“Save picture”可导出计算结果。

## 注意事项
- 流域面要素需添加一个名为“Name”的字符串字段，并赋好名字。
- 一次性最多只能计算15个流域的面积高程积分曲线。

## 引用说明
使用该工具发表的成果请标注引用：
J.V. Pérez-Peña, J.M. Azañón, A. Azor, CalHypso: An ArcGIS extension to calculate hypsometric curves and their statistical moments. Applications to drainage basin analysis in SE Spain, Computers & Geosciences, 2009, 35(6): 1214-1223.

## 致谢
感谢J.V. Pérez-Peña教授的慷慨帮助，使得该工具能够被广泛分享和使用。

## 下载链接

[CalHypso用于计算面积高程积分HI曲线的ArcGis扩展工具](https://pan.quark.cn/s/35ea1b4b7672)