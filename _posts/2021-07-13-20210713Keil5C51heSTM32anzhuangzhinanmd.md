---
layout: post
title: "Keil5C51和STM32安装指南"
date:   2020-02-01
tags: [点击,安装,Keil5,Next,C51]
comments: true
author: admin
---
# Keil5(C51和STM32)安装指南

本资源文件提供了详细的Keil5集成开发环境（IDE）安装指南，适用于C51和STM32微控制器的开发。通过本指南，您可以轻松地在Windows系统上安装和配置Keil5，以便进行嵌入式系统的开发。

## 安装步骤概述

### 第一步：安装MDK
1. 下载Keil5的压缩包并解压。
2. 右键以管理员身份运行`mdk514.exe`文件。
3. 点击“Next”。
4. 勾选“I agree”，点击“Next”。
5. 更改软件安装路径和器件包安装路径。
6. 填写用户信息（可随意填写），点击“Next”。
7. 开始安装。
8. 取消勾选，点击“Finish”。
9. 关闭弹出的窗口。

### 第二步：激活MDK
1. 在桌面上右击Keil5，以管理员身份运行。
2. 点击“File”，选择“License Management”。
3. 复制CID。
4. 在安装文件夹中右键以管理员身份运行`keygen.exe`文件。
5. 粘贴CID码，选择Target为ARM，点击“Generate”生成激活码。
6. 复制生成的激活码，粘贴在“New License ID Code”处，点击“Add LIC”，即可成功激活MDK。

### 第三步：安装STM32芯片包
1. 在安装文件夹中点击`Keil_STM32F1xx_DFP.2.2.0.pack`。
2. 等待安装完成，点击“Finish”。

### 第四步：安装C51单片机
1. 在安装文件夹中点击C51文件夹，右键以管理员身份运行`c51v959.exe`文件。
2. 点击“Next”。
3. 勾选“I agree to”，点击“Next”。
4. 在弹出的界面中会自动安装在安装Keil的路径，点击“Next”。
5. 用户信息不变，点击“Next”。
6. 等待安装完成，点击“Finish”。

### 第五步：激活C51单片机
1. 在桌面上右击Keil5，以管理员身份运行。
2. 点击“File”，选择“License Management”。
3. 复制CID。
4. 在安装文件夹中右键以管理员身份运行`keygen.exe`文件。
5. 粘贴CID码，选择Target为C51，点击“Generate”生成激活码。
6. 复制生成的激活码，粘贴在“New License ID Code”处，点击“Add LIC”，即可成功激活C51。

### 第六步：安装完成
确保所有步骤正确操作，Keil5即可同时支持STM32与C51的开发。

## 注意事项
- 安装过程中请确保网络连接稳定，以便顺利下载所需的芯片包。
- 安装路径建议选择非系统盘，以避免权限问题。
- 激活过程中请确保使用正版激活码，避免使用非法激活工具。

通过本指南，您可以顺利完成Keil5的安装和配置，开始您的嵌入式开发之旅。

## 下载链接

[Keil5C51和STM32安装指南](https://pan.quark.cn/s/c685757b6403)