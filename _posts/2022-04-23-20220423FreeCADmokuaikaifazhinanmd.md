---
layout: post
title: "FreeCAD模块开发指南"
date:   2020-07-05
tags: [FreeCAD,src,Base,3.2,3.5]
comments: true
author: admin
---
# FreeCAD模块开发指南

## 资源文件介绍

### 标题
FreeCAD开发指南(FreeCAD_Mod_Dev_Guide__20170101-1)

### 描述
本资源文件是FreeCAD源代码的模块开发者指南，由Qingfeng Xia编写，网址为http://www.iesensor.com。该指南的版本历史如下：

- 2015-09-18：版本0.1，适用于FreeCAD 0.16-dev
- 2016-09-18：版本0.2，适用于FreeCAD 0.17-dev

本书的许可证与FreeCAD文档的许可证相同，采用CC-BY 3.0。

## 内容概述

### 1. FreeCAD概述与架构
- 1.1 介绍FreeCAD
- 1.2 关键特性
- 1.3 软件架构
  - 1.3.1 关键软件库
  - 1.3.2 Python与C++混合编程
  - 1.3.3 GPL代码不会包含在安装程序中
- 1.4 3D模型的渲染方式
  - 1.4.1 3D可视化库的选择
  - 1.4.2 FreeCAD论坛上关于3D渲染库选择的讨论
- 1.5 FreeCAD路线图
  - 1.5.1 保持与主要组件的更新
  - 1.5.2 C++11
  - 1.5.3 Pyside 2项目（适用于Qt 5.x）

### 2. FreeCAD源代码的组织
- 2.1 FreeCAD的构建系统
  - 2.1.1 src/cMake/SMesh.cMake的分析
- 2.2 FreeCAD源文件夹中的文件和文件夹列表
- 2.3 FreeCAD Mod文件夹中的模块列表
- 2.4 学习路径
- 2.5 学习OpenInventor/Coin3D
  - 2.5.1 OpenInventor在FreeCAD的ViewProvider中的应用
  - 2.5.2 OpenInventor/Coin3D中的重要类
  - 2.5.3 窗口系统集成
  - 2.5.4 Pivy：Coin3D的Python封装

### 3. Base App和Main模块
- 3.1 Base文件夹中的头文件列表
  - 3.1.1 常用的头文件
  - 3.1.2 在try-catch块中正确使用Sequencer
  - 3.1.3 字符串编码utf8与wchar_t QString的转换
- 3.2 类型BaseClass PyObjectBase
  - 3.2.1 类型系统
  - 3.2.2 src/Base/BaseClass.h
  - 3.2.3 src/Base/PyObjectBase.h
  - 3.2.4 src/Base/Persistence.h
  - 3.2.5 GeoFeature：所有几何文档对象的基类
- 3.3 物理量的单位方案
  - 3.3.1 src/Base/Unit.h
  - 3.3.2 src/Base/Quantity.h
- 3.4 App文件夹中的头文件列表
- 3.5 属性框架
  - 3.5.1 属性的命名与PropertyEditor
  - 3.5.2 src/App/PropertyStandard.h
  - 3.5.3 PropertyEnumeration（见src/App/Enumeration.h）
  - 3.5.4 几何相关的属性
  - 3.5.5 文件相关的属性

## 下载说明

本仓库提供FreeCAD模块开发指南的下载，文件名为`FreeCAD_Mod_Dev_Guide__20170101-1`。请根据需要下载并参考。

## 下载链接

[FreeCAD模块开发指南](https://pan.quark.cn/s/53f5e3a17175)