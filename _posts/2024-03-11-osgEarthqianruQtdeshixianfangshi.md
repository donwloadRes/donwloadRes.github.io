---
layout: post
title: "osgEarth嵌入Qt的实现方式"
date:   2021-08-06
tags: [Qt,osgEarth,设置,嵌入,osgqt]
comments: true
author: admin
---
# osgEarth嵌入Qt的实现方式

## 简介

本资源文件提供了将osgEarth嵌入到Qt应用程序中的实现方式。通过本资源，开发者可以学习如何在Qt环境中集成osgEarth，并实现三维地理信息系统的显示和交互。

## 环境配置

- **开发环境**: VS2019 + QT5.9.8 + OSG3.6.5 + OSGEARTH3.1
- **前提条件**:
  1. 已经编译好了OSG以及OSGEARTH的运行时库。
  2. 关键的osgqt的3个类（osgqt太难编译了，这里提取它的3个类直接引进我们的工程）。

## 实现步骤

### 1. 新建工程

- 建立QT GUI工程，关键点：模块选择OPENGL。

### 2. 工程配置

- **添加osgqt的三个类**
- **工程属性配置**:
  - VC++目录下的可执行文件目录、包含目录、库目录。
  - 链接器输入下的附加依赖项。

### 3. 主函数代码

- 包含必要的头文件，如`QtWidgets/QMainWindow`、`osgDB/ReadFile`等。
- 初始化osgViewer、设置模型、配置图形环境特性、设置照相机等。

### 4. 初始化osgEarth

- 初始化mapNode、设置osgEarth操作器、获取地球半径并设置视点。

### 5. 初始化天空

- 获取当前时间，初始化天空，设置黑夜明暗程度。

### 6. 界面初始化

- 设置ui布局，将osgQt::GraphicsWindowQt嵌入到Qt窗口中。

### 7. 屏幕刷新初始化

- 使用QTimer定时更新帧。

## 使用说明

1. 下载资源文件并解压。
2. 按照上述环境配置要求，配置开发环境。
3. 将资源文件中的代码集成到你的Qt工程中。
4. 根据需要调整代码，实现自定义功能。

## 注意事项

- 确保所有依赖库已正确配置。
- 根据实际需求调整代码中的路径和参数。

通过本资源文件，开发者可以快速掌握osgEarth在Qt中的集成方法，并在此基础上进行进一步的开发和优化。

## 下载链接

[osgEarth嵌入Qt的实现方式分享](https://pan.quark.cn/s/836a12997e64)