---
layout: post
title: "Keil_v5软件安装指南及项目工程创建"
date:   2020-12-26
tags: [文件夹,Keil,创建,文件,v5]
comments: true
author: admin
---
# Keil_v5软件安装指南及项目工程创建

本资源文件提供了详细的Keil_v5软件安装指南以及项目工程创建步骤。通过本指南，您可以轻松完成Keil_v5的安装，并创建一个完整的项目工程。

## 内容概述

1. **Keil_v5安装指南**
   - 安装包获取
   - 关闭防火墙
   - 打开资料文件
   - 双击运行MDK536.EXE
   - 双击运行keygen.exe文件
   - 破解完成

2. **项目工程创建**
   - 项目创建
   - 添加配置
   - 进入工程
   - 程序运行

## 详细步骤

### 1. Keil_v5安装指南

#### 安装包获取
- 获取Keil_v5的安装包，确保所有必要的文件齐全。

#### 关闭防火墙
- 在安装过程中，建议暂时关闭防火墙以避免安装过程中的网络干扰。

#### 打开资料文件
- 检查文件夹中的文件是否有缺失，确保包含CMS开发资料压缩包、JLink仿真软件、keygen破解软件、MDK536.exe安装程序等。

#### 双击运行MDK536.EXE
- 点击“Next”进行下一步安装。
- 更改安装目录路径至D盘下。
- 点击“Next”等待安装完成。
- 关闭程序。
- 以管理员身份运行Keil uVersion5。
- 打开后，复制License Management的右侧CID。

#### 双击运行keygen.exe文件
- 在文件夹中找到破解工具。
- 更改Target为ARM。
- 选择Prof Developers Kit(PLUS)。
- 粘贴上述复制的CID，点击Generate。
- 复制生成的代码，并粘贴到Keil5的下述路径，点击AddLIC。
- 破解完成后提示Support Period至Dec 2032。

### 2. 项目工程创建

#### 项目创建
- 在D盘下创建一个存放项目的工程文件夹。
- 在ProjectWork文件夹内创建KeilProject文件夹。
- 在KeilProject文件夹内创建BAT32G137芯片型号工程文件夹。
- 在BAT32G137文件夹内创建Project文件夹，用来存放开发该项目的所有文件。
- 点击Project按钮下的New uVision Project，找到BAT32G137文件夹，在该目录下创建一个项目名称文件夹为project。
- 双击进入project文件夹下，将目标uVision project放入该路径下。
- 文件名写为：BAT32G137，点击保存。
- 进入下图页面，勾选BAT32G137芯片包缺失文件，由Keil提供，点击OK。

#### 添加配置
- 复制BAT32G137PACK包下的例程配置文件，并在复制前将文件夹属性取消【只读】，点击确定。
- 在project文件夹中，CMSIS、Device、Driver为复制文件，OutPut、Source、Doc为自己创建的文件。
- Listings、Objects、RTE文件夹为创建新工程自动生成文件。

#### 进入工程
- 使用Keil软件运行BAT32G137.uvprojx文件，文件类型为【礦ision5 Project】。
- 进入工程后，将所需要的项目文件导入到工程，导入完成后在左侧会显示导入的项目文件。
- 导入完成后，点击配置【每项】：Target配置、Output配置、C/C++配置、Include Paths配置、Debug配置。

#### 程序运行
- 在mian.c文件中写入测试代码。

## 总结

通过本指南，您可以顺利完成Keil_v5的安装及项目工程的创建。希望本指南对您的学习和开发有所帮助。

## 下载链接

[Keil_v5软件安装指南及项目工程创建分享](https://pan.quark.cn/s/48acbaa07bf5)