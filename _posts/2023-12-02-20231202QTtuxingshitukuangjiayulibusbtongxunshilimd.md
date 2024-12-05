---
layout: post
title: "QT图形视图框架与libusb通讯示例"
date:   2022-03-23
tags: [视图,libusb,QT,框架,图形]
comments: true
author: admin
---
# QT图形视图框架与libusb通讯示例

## 项目描述
本项目通过Qt的图形视图框架（QGraphicsView）进行2D绘图，并调用libusb进行通讯。软件架构主要由两部分组成：
1. libusb的调用和使用；
2. Qt图形视图框架的基本使用。

## 安装教程
1. 使用QT打开工程文件；
2. 修改.pro文件中的库路径；
3. 设置kits，编译运行。

## 使用说明
### libusb部分
主要介绍了libusb的设备打开，端口打开，以及中断方式传输数据。

### Qt图形视图框架部分
主要介绍了Qt的视图框架QGraphicsView、QGraphicsScene和QGraphicsItems的基本使用。利用QT的视图框架进行了基本图形的绘制，比如画点、画线、画矩形等。

## 注意事项
确保libusb库路径正确，并且在编译前设置好相应的kits。

## 下载链接

[QT图形视图框架与libusb通讯示例](https://pan.quark.cn/s/603d682875c5)