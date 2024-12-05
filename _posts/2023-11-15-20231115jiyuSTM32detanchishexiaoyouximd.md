---
layout: post
title: "基于STM32的贪吃蛇小游戏"
date:   2022-02-18
tags: [贪吃蛇,游戏,链表,界面,STM32]
comments: true
author: admin
---
# 基于STM32的贪吃蛇小游戏

## 项目简介

本项目是一个基于STM32微控制器的贪吃蛇小游戏。通过使用C语言链表的方式来实现贪吃蛇的移动和增长，并将其移植到野火指南者开发板上，使其能够在3.2寸触摸屏上显示。游戏界面为240X240像素，贪吃蛇和食物的方格大小为6X6像素，游戏界面在程序中被视为40X40的坐标系。

## 主要功能

1. **贪吃蛇链表**：使用链表数据结构来管理贪吃蛇的身体节点，实现蛇的移动和增长。
2. **ADC模块**：利用ADC1的通道13（PC3）采集环境噪声数据，生成随机数来确定食物的位置。
3. **定时器中断**：通过4ms定时器中断检测按键状态，控制游戏的暂停和继续。

## 实际显示效果

- **暂停/继续功能**：通过触摸屏上的暂停键可以控制游戏的暂停或继续。
- **游戏结束提示**：当贪吃蛇超出界面边界或咬到自己时，界面会显示“Game over”的字样，点击屏幕任意地方可以重新开始游戏。

## 代码结构

- **贪吃蛇链表**：参考了其他算法的实现，通过链表管理蛇的身体节点。
- **ADC模块**：使用ADC采集环境噪声数据，生成随机数来确定食物的位置。
- **定时器中断**：在4ms定时器中断中检测按键状态，控制游戏的暂停和继续。

## 使用说明

1. 将代码下载并导入到STM32开发环境中。
2. 将代码烧录到野火指南者开发板上。
3. 连接3.2寸触摸屏，启动游戏。
4. 通过触摸屏控制贪吃蛇的移动方向，吃到食物后蛇的长度会增加。
5. 当蛇超出界面边界或咬到自己时，游戏结束，点击屏幕任意地方可以重新开始游戏。

## 注意事项

- 本项目使用的是标准库，如果需要使用HAL库，请参考相关文档进行移植。
- 游戏界面为240X240像素，贪吃蛇和食物的方格大小为6X6像素，请确保屏幕分辨率匹配。

## 贡献

欢迎对本项目进行改进和优化，提交Pull Request或Issue。

## 许可证

本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[基于STM32的贪吃蛇小游戏](https://pan.quark.cn/s/010ecebea8fa)