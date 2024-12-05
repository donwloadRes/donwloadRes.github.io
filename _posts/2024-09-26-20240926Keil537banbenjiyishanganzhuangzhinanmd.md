---
layout: post
title: "Keil 537版本及以上安装指南"
date:   2022-05-17
tags: [Keil,安装,点击,版本,编译器]
comments: true
author: admin
---
# Keil 5.37版本及以上安装指南

本资源文件提供了Keil 5.37及以上版本的安装步骤，并解决了“Default Compiler Version 5”不可用的问题。以下是详细的安装和配置指南。

## 前言

在Keil 5.37及以上版本中，默认编译器中不再默认安装Compiler Version 5，因此需要自行安装。本文以Keil 5.38a版本为例，详细说明安装所需步骤。

## 准备事项

在开始安装之前，请准备以下三个安装包：
1. Keil 5.38a安装包
2. Keil 2032注册机（支持正版）
3. V5版本编译器（推荐v5.06 update 7(build 960)版本）

## 安装步骤

### 1. 安装Keil

1. 运行MDK5.38a.exe安装包。
2. 按照安装向导的提示，点击“Next”进行安装。
3. 在安装路径选择界面，选择合适的安装位置，建议使用纯英文路径。
4. 填写个人信息后，继续点击“Next”完成安装。
5. 安装完成后，点击“Finish”。

### 2. 注册Keil

1. 关闭系统防火墙（如Win11的Defender），确保注册机运行时不会被误报病毒删除。
2. 以管理员身份运行Keil，并打开“File -> License Management”。
3. 打开Keil注册机，按照以下步骤操作：
   - 复制CID到注册机。
   - 选择Target为ARM。
   - 选择Professional版本。
   - 点击Generate生成注册码。
   - 复制注册码到Keil License中。
   - 点击Add LIC按钮。
   - 点击Close。

### 3. 安装V5编译器

1. 解压V5编译器压缩包，并重启电脑。
2. 找到Keil的Core安装路径，打开其中的ARM文件夹。
3. 在该目录下新建空文件夹ARMCC，用于安装V5编译器。
4. 运行V5安装包路径下的setup.exe，按照向导提示完成安装。
5. 安装完成后，点击“Finish”。

### 4. 配置编译器

1. 打开Keil，点击“魔术棒”图标，找到Target项。
2. 检查ARM Compiler是否为Use default compiler version 5或V5.06 xxxxxxx build960。
3. 如果不是，手动选择合适的编译器版本。
4. 点击OK完成配置。

## 结束

至此，Keil 5.37及以上版本的安装和配置已完成。如果遇到任何问题，欢迎参考本文进行排查。

## 下载链接

[Keil5.37版本及以上安装指南](https://pan.quark.cn/s/0692c4267770)