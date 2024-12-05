---
layout: post
title: "如何在Windows家庭版中启用组策略"
date:   2022-10-24
tags: [Windows,组策略,家庭版,启用,编辑器]
comments: true
author: admin
---
# 如何在Windows家庭版中启用组策略

## 简介
在Windows家庭版中，默认情况下并不包含组策略编辑器（Group Policy Editor），这使得用户无法直接通过组策略来定制系统设置。然而，通过一些简单的步骤，我们可以在Windows家庭版中启用组策略编辑器，从而获得更多的系统配置选项。

## 操作步骤

### 1. 创建批处理文件
首先，在桌面上新建一个文本文件，并将以下代码复制到该文本文件中：

```cmd
@echo off
pushd "%~dp0"
dir /b C:\Windows\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~3*.mum >List.txt
dir /b C:\Windows\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~3*.mum >>List.txt
for /f %%i in ('findstr /i . List.txt 2^>nul') do dism /online /norestart /add-package:"C:\Windows\servicing\Packages\%%i"
pause
```

### 2. 保存文件
将文件另存为“启用组策略.cmd”，确保文件类型选择为“所有文件”，扩展名为“.cmd”。

### 3. 以管理员身份运行
右键点击刚刚创建的“启用组策略.cmd”文件，选择“以管理员身份运行”。等待安装完成，按任意键退出。

### 4. 验证组策略编辑器
安装完成后，打开运行对话框（Win + R），输入“gpedit.msc”并按回车，此时你应该能够看到组策略编辑器已经成功启用。

## 注意事项
- 在执行此操作之前，建议创建系统还原点，以便在出现问题时可以恢复系统。
- 此方法适用于Windows家庭版，其他版本如专业版、企业版等已经包含组策略编辑器，无需此操作。

通过以上步骤，你可以在Windows家庭版中成功启用组策略编辑器，从而获得更多的系统配置和管理选项。

## 下载链接

[如何在Windows家庭版中启用组策略分享](https://pan.quark.cn/s/3c83b1001af0)