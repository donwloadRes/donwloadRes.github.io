---
layout: post
title: "Win10下Keil5的C51和ARM共存的开发环境配置"
date:   2023-09-07
tags: [C51,ARM,Keil,MDK,安装]
comments: true
author: admin
---
# Win10下Keil5的C51和ARM共存的开发环境配置

## 概述
在学习和开发嵌入式系统时，经常会遇到需要同时使用51单片机和ARM单片机的情况。由于这两种单片机的架构不同，开发环境也有所不同。为了方便开发，本文将详细介绍如何在Windows 10系统下配置Keil5，使其能够同时支持C51和ARM的开发环境。

## 正文

### 1. 安装 C51
1. 下载最新版本的Keil C51软件包。
2. 双击安装文件 `C51V954.exe` 并运行。
3. 按照安装向导的提示，选择安装路径并完成安装。

### 2. 安装 MDK
1. 下载最新版本的Keil MDK软件包。
2. 双击安装文件 `MDK536.exe` 并运行。
3. 按照安装向导的提示，选择安装路径并完成安装。

### 3. C51 和 MDK 共存
1. 打开C51的安装目录和MDK的安装目录。
2. 将C51目录下的 `C51` 文件夹复制到MDK目录下。
3. 将C51目录下的 `UV4` 文件夹中的所有文件复制到MDK目录下的 `UV4` 文件夹中。
4. 将C51目录下的 `TOOLS.INI` 文件内容复制到MDK目录下的 `TOOLS.INI` 文件末尾。

### 4. 注册
1. 关闭防火墙和病毒防护软件。
2. 以管理员身份运行破解软件。
3. 打开MDK目录下的 `UV4` 文件夹中的 `UV4.exe`，点击 `File` 菜单中的 `License Management`。
4. 复制CID并粘贴到破解软件中，选择对应的Target（C51或ARM），生成License并添加到Keil中。

### 5. 安装 STM32 PACK
1. 打开Keil软件，点击 `Pack Installer` 图标。
2. 选择 `File` 菜单中的 `Import`，导入下载好的STM32 PACK文件。
3. 等待安装完成后关闭 `Pack Installer`。

### 6. 更改配色
1. 复制 `global.prop` 文件到Keil的安装路径下。
2. 重启Keil，配色更改成功。

## 结语
通过以上步骤，您可以在Windows 10系统下成功配置Keil5，使其同时支持C51和ARM的开发环境。这样，您就可以在一个开发环境中同时编写和编译51单片机和ARM单片机的程序，大大提高了开发效率。

## 下载链接

[Win10下Keil5的C51和ARM共存的开发环境配置分享](https://pan.quark.cn/s/2467f211138b)