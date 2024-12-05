---
layout: post
title: "STM32打地鼠游戏项目介绍"
date:   2024-04-25
tags: [地鼠,触摸屏,任务,游戏,出洞]
comments: true
author: admin
---
# STM32打地鼠游戏项目介绍

## 项目概述
本项目基于STM32F103ZET6芯片和UCOSIII实时操作系统，实现了一个简单的打地鼠游戏。游戏通过2.8寸触摸屏进行操作，玩家需要在规定时间内点击屏幕上随机出现的地鼠，以获得分数。

## 游戏规则
- 每800ms，一只地鼠会完成出洞和回洞两次操作。
- 如果在地鼠出洞时成功点击到地鼠，则加一分。

## 硬件需求
- STM32F103ZET6芯片
- 2.8寸触摸屏

## 编程方式
- 使用UCOSIII实时操作系统进行编程

## 编程思路及主要代码
1. **背景设置及任务创建**：
   - 设置3*3方格背景。
   - 创建三个任务：开始任务、地鼠控制任务、触摸屏控制任务。
   - 创建一个软件定时器。

2. **开始任务**：
   - 创建地鼠控制任务和触摸屏控制任务，并删除任务自身。

3. **地鼠出洞控制任务**：
   - 利用软件定时器回调函数产生随机数，控制地鼠出洞的坑位。
   - 每400ms设置一个任务调度点，第一个调度点地鼠出现，第二个调度点地鼠消失。

4. **触摸屏控制任务**：
   - 如果触碰到对应方格并且打到地鼠，得分加一。

## 基础代码扩展
- 设置一个另外颜色的地鼠，打到减分。
- 如果分数为负，显示游戏结束。
- 设置关卡，关卡越高，地鼠出洞回洞越快，难度越大。

## 实验现象
- 游戏运行后，地鼠会在随机位置出现和消失，玩家通过触摸屏点击地鼠进行游戏。

## 其他说明
- 由于要考研了，所以只做了个简易版的练练手，以下是我想的一些思路仅供参考。
- 大家可以集思广益，做一个超强版打地鼠，哈哈哈。

## 下载链接

[STM32打地鼠游戏项目介绍](https://pan.quark.cn/s/893b0a250415)