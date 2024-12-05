---
layout: post
title: "STM32开发环境搭建指南：Keil5安装教程"
date:   2023-05-18
tags: [STM32,安装,Keil5,点击,MDK]
comments: true
author: admin
---
# STM32开发环境搭建指南：Keil5安装教程

本资源文件提供了详细的STM32开发环境搭建指南，特别是关于Keil5的安装步骤。通过本指南，您可以轻松完成STM32开发环境的搭建，为后续的开发工作打下坚实的基础。

## 内容概述

1. **MDK安装包获取**
   - 从官网下载MDK-Arm安装包。
   - 填写个人信息并提交，进入软件下载界面。
   - 点击MDK535.EXE开始下载软件。

2. **注册机获取**
   - 获取Keil5的注册机，用于激活软件。

3. **STM32开发支持包获取**
   - 从官网下载STM32相关的MDK支持包。
   - 本次环境搭建将同时安装STM32F1和F4系列的支持包。

4. **MDK安装**
   - 双击MDK535.EXE文件进入安装界面，选择Next。
   - 根据需求选择安装路径，Core为Keil软件的安装路径，Pack为软件开发支持包的存放路径。
   - 填写Customer Information中的内容，可以随意填写。
   - 等待安装完成，安装过程中会自动安装ST-Link驱动。
   - 安装完成后，取消勾选Show Release Notes，点击Finish。

5. **STM32开发支持包安装**
   - 依次双击Pack包，点击安装即可。

6. **MDK注册**
   - 找到Keil5图标，右键以管理员模式运行。
   - 在Keil 5软件中点击File->License Management打开注册窗口。
   - 将CID复制到剪切板，找到注册机并右键管理员运行。
   - 复制CID到注册机的CID输入栏中，Target选择Arm，点击Generate按钮生成激活码。
   - 将激活码粘贴至New License ID Code输入栏中，点击Add LIC按钮，注册成功。

## 注意事项

- 若没有以管理员模式运行Keil5软件，则在点击Add LIC时会报错。
- 本文中所涉及的软件安装包相关资源已上传百度云盘，方便大家下载。

通过本指南，您可以顺利完成STM32开发环境的搭建，为后续的开发工作提供便利。

## 下载链接

[STM32开发环境搭建指南Keil5安装教程](https://pan.quark.cn/s/779dd9f661d5)