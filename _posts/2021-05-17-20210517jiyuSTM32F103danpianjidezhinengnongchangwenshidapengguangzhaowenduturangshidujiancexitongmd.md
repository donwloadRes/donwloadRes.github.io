---
layout: post
title: "基于STM32F103单片机的智能农场温室大棚光照温度土壤湿度检测系统"
date:   2021-09-23
tags: [土壤湿度,设定值,温度,光照强度,检测]
comments: true
author: admin
---
# 基于STM32F103单片机的智能农场温室大棚光照温度土壤湿度检测系统

## 简介
本资源文件提供了一个基于STM32F103单片机的智能农场温室大棚光照温度土壤湿度检测系统的完整解决方案。该系统通过集成多种传感器，实现了对温室大棚内光照强度、温度和土壤湿度的实时监测与控制。

## 系统功能
1. **光照强度检测与控制**：
   - 通过光敏电阻检测光照强度，并将数据通过AD转换后显示在LCD1602液晶屏上。
   - 用户可以通过按键设定光照强度的阈值，当光照低于设定值时，系统会自动开启高亮LED灯进行补光；当光照高于设定值时，LED灯关闭。

2. **温度检测与控制**：
   - 使用DS18B20传感器检测温度，并将实时温度显示在LCD1602液晶屏上。
   - 用户可以通过按键设定温度阈值，当温度超过设定值时，系统会自动启动风扇进行降温；当温度低于设定值时，风扇停止。

3. **土壤湿度检测与控制**：
   - 通过土壤湿度传感器检测土壤湿度，并将湿度值实时显示在LCD1602液晶屏上。
   - 用户可以通过按键设定土壤湿度阈值，当土壤湿度低于设定值时，系统会自动启动继电器控制水泵进行浇水；当土壤湿度高于设定值时，水泵停止。

## 系统组成
- **核心板**：基于STM32F103C8T6单片机。
- **显示模块**：LCD1602液晶显示屏。
- **传感器**：光敏电阻、DS18B20温度传感器、土壤湿度传感器。
- **控制模块**：风扇控制、继电器控制、高亮LED灯补光。
- **输入模块**：按键控制。

## 使用说明
1. **硬件连接**：按照原理图连接各传感器和控制模块到STM32F103C8T6核心板。
2. **软件配置**：将提供的源代码烧录到STM32F103C8T6单片机中。
3. **系统启动**：上电后，系统将自动开始监测光照强度、温度和土壤湿度，并根据设定的阈值进行自动控制。

## 资源内容
- 系统原理图
- 源代码
- 使用说明文档

## 适用场景
本系统适用于智能农场、温室大棚等需要实时监测和控制环境参数的场景，能够有效提高农业生产的自动化水平和管理效率。

## 注意事项
- 请确保硬件连接正确，避免短路或接错线。
- 在设定阈值时，请根据实际需求进行调整，以确保系统的正常运行。

## 联系我们
如有任何问题或建议，请联系我们：[联系方式]

## 下载链接

[基于STM32F103单片机的智能农场温室大棚光照温度土壤湿度检测系统](https://pan.quark.cn/s/30657bcf61d8)