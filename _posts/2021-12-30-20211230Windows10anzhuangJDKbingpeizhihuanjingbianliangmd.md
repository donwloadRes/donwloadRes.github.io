---
layout: post
title: "Windows 10 安装 JDK 并配置环境变量"
date:   2020-06-14
tags: [JDK,安装,环境变量,Windows,点击]
comments: true
author: admin
---
# Windows 10 安装 JDK 并配置环境变量

本文将详细介绍如何在 Windows 10 操作系统上安装 JDK（Java Development Kit）并配置环境变量。通过本文的指导，您将能够顺利完成 JDK 的安装，并确保系统能够正确识别和使用 Java 环境。

## 1. 下载 JDK

首先，您需要下载适用于 Windows 10 的 JDK 安装包。您可以通过以下步骤获取 JDK：

1. 访问 Oracle 官方网站或其他可信的 JDK 下载源。
2. 选择适合您操作系统的 JDK 版本（通常选择 Windows x64 版本）。
3. 下载 JDK 安装包。

## 2. 安装 JDK

下载完成后，按照以下步骤安装 JDK：

1. 双击下载的 JDK 安装包，启动安装程序。
2. 按照安装向导的提示，选择安装路径（建议使用默认路径）。
3. 完成安装后，点击“关闭”按钮退出安装程序。

## 3. 配置环境变量

安装完成后，需要配置系统的环境变量，以便系统能够识别并使用 JDK。以下是配置步骤：

1. 右键点击“此电脑”或“计算机”图标，选择“属性”。
2. 在左侧菜单中选择“高级系统设置”。
3. 在弹出的窗口中，点击“环境变量”按钮。
4. 在“系统变量”部分，找到并选择“Path”变量，然后点击“编辑”。
5. 在“编辑环境变量”窗口中，点击“新建”按钮，添加 JDK 的安装路径（例如：`C:\Program Files\Java\jdk1.8.0_281\bin`）。
6. 确认所有窗口中的更改，并依次点击“确定”按钮关闭所有窗口。

## 4. 验证安装

完成上述步骤后，您可以通过以下方式验证 JDK 是否安装成功：

1. 打开命令提示符（按 `Win + R`，输入 `cmd`，然后按回车）。
2. 输入 `java -version` 命令，如果显示 Java 版本信息，则表示 JDK 安装成功。

## 5. 附录

如果您在下载 JDK 时遇到困难，可以访问以下网盘地址获取 JDK 安装包：

- 网盘下载地址：[此处省略网盘地址]

通过以上步骤，您应该能够成功在 Windows 10 上安装 JDK 并配置环境变量。如果在安装过程中遇到任何问题，请参考相关文档或寻求技术支持。

## 下载链接

[Windows10安装JDK并配置环境变量](https://pan.quark.cn/s/387d6b5c94da)