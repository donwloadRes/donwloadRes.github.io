---
layout: post
title: "Keil uVision5 安装指南  51单片机篇"
date:   2020-07-13
tags: [点击,Keil,安装,uVision5,选择]
comments: true
author: admin
---
# Keil uVision5 安装指南 - 51单片机篇

本资源文件提供了Keil uVision5的安装指南，特别适用于51单片机的开发工作。以下是详细的安装步骤和配置说明。

## 一、Keil uVision5 下载安装

1. 下载安装包：将文件下载到电脑上。
2. 运行安装程序：点击 `C51-V957.exe` 文件，以管理员身份运行。
3. 同意许可协议：勾选 `I agree to···`，点击 `Next`。
4. 选择安装路径：点击 `Browse` 选择安装路径（不推荐放在C盘），然后点击 `Next`。
5. 填写信息：填写必要信息后，点击 `Next` 开始安装。
6. 安装完成：点击 `Finish` 完成安装。

## 二、Keil uVision5 软件破解

1. 以管理员身份运行 Keil uVision5。
2. 打开许可证管理：点击 `File`，选择 `Licence Management`。
3. 复制 CID：复制 `CID` 代码。
4. 运行破解工具：打开安装包中的 `keygen_new2032.exe`，以管理员身份运行。
5. 生成许可证：粘贴复制的 `CID`，点击 `Generate`，复制生成的内容。
6. 添加许可证：返回 Keil uVision5，将复制的内容粘贴在 `LIC` 栏中，点击 `Add LIC`。
7. 验证破解：若提示绿化成功，则说明软件破解成功。

## 三、STC官方库添加

1. 打开程序烧入软件：双击打开安装包中的程序烧入软件。
2. 添加型号和头文件：选择 `Keil仿真设置`，点击 `添加型号和头文件···`。
3. 选择安装目录：选择 Keil uVision5 的安装目录，点击 `确定`。
4. 成功添加：成功添加STC官方库。

## 四、Keil相关配置

### 1. 中文显示配置

- 设置中文显示：点击 `Edit`，选择 `Configuration`，点击 `Editor`，选择中文简体，单击 `OK`。

### 2. 消除定义但未被使用函数的警告配置

- 配置消除警告：点击 `魔术棒`，选择 `Device`，勾选 `Use Extended`，点击 `OK`。再次点击 `魔术棒`，选择 `LX51 Misc`，输入 `REMOVEUNUSED`，点击 `OK`，完成配置。

## 五、程序烧入软件的使用

1. 选择芯片型号：选择 `STC89C51`。
2. 打开程序文件：点击 `打开程序文件`，选择需要运行的 `.hex` 文件。
3. 下载/编程：点击 `下载/编程`，确保单片机与电脑正常连接。

通过以上步骤，您可以顺利完成Keil uVision5的安装、破解、配置以及程序烧入软件的使用。希望本指南对您的51单片机开发工作有所帮助。

## 下载链接

[KeiluVision5安装指南-51单片机篇](https://pan.quark.cn/s/cc63ca7f7cf0)