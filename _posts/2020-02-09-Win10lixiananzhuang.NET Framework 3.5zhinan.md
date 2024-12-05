---
layout: post
title: "Win10离线安装.NET Framework 3.5指南"
date:   2022-09-21
tags: [离线,安装,NET,Windows,Framework]
comments: true
author: admin
---
# Win10离线安装.NET Framework 3.5指南

## 概述

本文档旨在为无法在线安装或需要批量部署的用户提供详细的离线安装.NET Framework 3.5至Windows 10系统的步骤。内含直接下载的cab格式离线安装包，确保您能在没有互联网连接的情况下顺利完成老版本.NET框架的安装，这对于运行特定的老旧软件或满足系统需求至关重要。

## 准备工作

- **下载离线安装包**: 请访问相关资源页面获取cab格式的安装包。
- **适用系统**: 此方法适用于Windows 10所有受支持的版本。

## 安装步骤

### 步骤1: 准备安装文件
- 将下载的`.cab`文件放置于C:\Windows目录下。

### 步骤2: 以管理员身份运行命令提示符
- 打开“命令提示符”作为管理员。可以通过搜索栏找到并右击选择“以管理员身份运行”。

### 步骤3: 执行安装命令
- 在命令提示符中输入以下命令，并按Enter键执行：
  
  ```cmd
  dism /online /Enable-Feature /FeatureName:NetFx3 /Source:"%windir%" /LimitAccess
  ```
  
  此命令会利用当前系统的cab文件离线激活.NET Framework 3.5特性。

### 步骤4: 等待安装完成
- 上述命令执行后，系统将处理安装请求。请耐心等待，直至看到成功消息。

### 步骤5: (可选)验证安装
- 安装结束后，可通过控制面板的“程序和功能”->“启用或关闭Windows功能”检查.NET Framework 3.5是否已成功启用。

## 注意事项
- 若您的系统缺少原始安装介质(SXS目录)，您可能需要使用Windows安装媒体或ISO文件中的SXS目录来替换上述命令中的`"%windir%"`部分，指向安装介质的正确路径。
- 请确保在执行命令前备份重要数据，尽管该过程相对安全。

## 结语

遵循以上步骤，即使在无网络的环境中，您也能轻松为Windows 10系统安装.NET Framework 3.5，确保软件的兼容性和功能性。希望这份指南对您的操作有所帮助。

## 下载链接

[Win10离线安装.NETFramework3.5指南分享](https://pan.quark.cn/s/c8ac4d960ea6)