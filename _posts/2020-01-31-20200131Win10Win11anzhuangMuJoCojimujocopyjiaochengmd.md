---
layout: post
title: "Win 10Win 11 安装 MuJoCo 及 mujocopy 教程"
date:   2020-05-11
tags: [mujoco,MuJoCo,py,安装,Windows]
comments: true
author: admin
---
# Win 10、Win 11 安装 MuJoCo 及 mujoco-py 教程

本资源文件提供了在Windows 10和Windows 11系统上安装MuJoCo及mujoco-py的详细教程。MuJoCo是一个物理模拟器，广泛用于机器人控制和强化学习等领域。mujoco-py是OpenAI提供的Python接口，允许用户通过Python 3使用MuJoCo。

## 安装前言

### 安装基础说明
本教程基于Windows系统，旨在方便后续强化学习算法的对比实验。目前大部分教程都是基于MuJoCo被DeepMind收购之前的版本，安装过程较为复杂，存在不少隐性坑。

### MuJoCo 说明
MuJoCo最初由美国华盛顿大学运动控制实验室主任、神经科学家Emo Todorov开发，于2015年通过创业公司Roboti LLC被打造成商业产品。2021年10月，DeepMind宣布收购MuJoCo物理模拟器，并承诺将其作为一个免费的、开源的、社区驱动的项目进行开发和维护。

### mujoco-py 说明
OpenAI官方提供的mujoco-py Github地址为：openai/mujoco-py。比较好的支持Windows 10 / Windows 11系统的版本是v1.50.1.0。

## 具体安装流程

### 安装文件分享
为防止网络故障等因素干扰，我将安装所需的全部文件都已打包上传至百度网盘中。

### 安装 Visual Studio Build Tools
这一部分的安装是整个过程中非常重要的一环，因为mujoco仿真引擎是基于C/C++的，所以每一次运行时实际上都是通过VS Build Tools进行编译转换。

### 安装 mjpro150 和 mujoco-py
这一部分可参考下述帖子，安装思路清晰，每一步都有对应的截图。

## 运行程序时的部分报错说明

### ImportError: DLL load failed while importing cymj
这个报错是因为Python的版本较高，自Python 3.8开始，在程序运行时只会加载trusted dlls。解决方案是对于Python 3.8及以上的Python版本，每次运行import mujoco_py指令前需要先运行下述三行命令。

### distutils.errors.DistutilsExecError
这个是非常常见的一个报错，具体是因为电脑上安装的路径名过长，包括Python安装路径名和vsbuildtools安装路径名。

### 其他报错
这篇安装博客还给出了报错的一个原因：Visual Studio、visual studio SDK没有和anaconda、python、pycharm安装在一个盘里。

## 安装教程的具体配置信息
日期：2022-07-25
操作系统：Windows 11
python版本：3.9.0
mujoco版本：mjpro150
mujoco-py版本：1.50.1.0
gym版本：0.13.0

希望本教程能帮助你在Windows系统上顺利安装MuJoCo及mujoco-py，并进行后续的强化学习实验。

## 下载链接

[Win10Win11安装MuJoCo及mujoco-py教程](https://pan.quark.cn/s/77be3f50473e)