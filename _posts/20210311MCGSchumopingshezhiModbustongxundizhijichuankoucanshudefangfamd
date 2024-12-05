---
layout: post
title: "MCGS触摸屏设置Modbus通讯地址及串口参数的方法"
date:   2021-01-21
tags: [Modbus,组态,MCGS,nAddr,设置]
comments: true
author: admin
---
# MCGS触摸屏设置Modbus通讯地址及串口参数的方法

本文详细介绍了如何使用MCGS组态软件的第三方定制驱动，设置Modbus通信参数，包括作为主站时的设置步骤，以及作为从站时的配置方法。涉及站号、波特率等关键参数的调整。

## 一、说明

MCGS(昆仑通态)组态软件原版Modbus驱动无法通过画面组态调用宏来设置Modbus通信相关参数，如站号、波特率、数据位、停止位、校验位等。但可以通过第三方定制版驱动来实现该功能，亲测有效。

## 二、屏幕做Modbus主站时相关设置

1. **下载安装第三方定制驱动程序**：点击下载，提取码：2mhr。
2. **新建测试工程**：并新建一个画面，画面布局如下。
3. **实时数据库设置**：在实时数据库里新建11个数值变量分别为nAddr、nBaudrate、nDatabit、nStopbit、nParity、nReturn和rAddr、rBaudrate、rDatabit、rStopbit、rParity。将组态画面左侧文本框依次关联nAddr、nBaudrate、nDatabit、nStopbit、nParity这几个变量，右侧标签依次关联rAddr、rBaudrate、rDatabit、rStopbit、rParity。
4. **组态设置按钮的按下脚本**：写入以下代码：
   ```
   '设置设备1的设备地址，设置地址值为nAddr的值，nAddr为数值型变量
   SetDevice(设备1, 6, "SetAddress(nAddr)")
   ```

## 三、注意事项

在操作前，务必了解所使用的硬件设备支持的Modbus协议版本和具体参数设置，确保设备间的通信顺利进行。

## 四、总结

通过第三方驱动提供的API接口，可以动态调整MCGS触摸屏的Modbus通信参数，确保设备间的通信顺利进行。

## 下载链接

[MCGS触摸屏设置Modbus通讯地址及串口参数的方法分享](https://pan.quark.cn/s/6ac0b76b31ea)