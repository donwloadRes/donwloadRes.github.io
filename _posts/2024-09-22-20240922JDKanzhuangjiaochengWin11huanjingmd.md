---
layout: post
title: "JDK安装教程（Win11环境）"
date:   2024-04-05
tags: [JDK,安装,环境变量,教程,Windows]
comments: true
author: admin
---
# JDK安装教程（Win11环境）

本仓库提供了一份详细的JDK安装教程，适用于Windows 11操作系统。该教程涵盖了从下载JDK到配置环境变量的全过程，帮助用户顺利完成JDK的安装和配置。

## 目录
1. 下载JDK
2. 安装JDK
3. 配置环境变量
4. 检验是否安装成功

### 1. 下载JDK
通过官方链接进入Oracle官网，选择Java 11版本，下载适用于Windows的JDK安装包。

### 2. 安装JDK
解压下载好的JDK压缩文件，将其复制到你想要存放的文件夹中。

### 3. 配置环境变量
- 右键点击“此电脑”，选择“属性”。
- 选择“高级系统设置”。
- 点击“环境变量”。
- 新建系统变量，变量名为`JAVA_HOME11`，变量值为JDK文件夹路径。
- 编辑`Path`变量，添加以下两个环境变量：
  - `%JAVA_HOME11%\bin`
  - `%JAVA_HOME11%\bin\jre`

### 4. 检验是否安装成功
- 按下`Win键+R`，输入`cmd`，回车打开命令提示符。
- 输入`java -version`，查看JDK版本。
- 输入`javac -version`，查看JRE版本。

如果命令行中显示了相应的版本信息，则表示JDK安装成功。如果出现错误提示，请检查环境变量配置是否正确，或尝试重启计算机。

---

通过以上步骤，您应该能够顺利在Windows 11系统上安装并配置JDK。如果在安装过程中遇到任何问题，欢迎在仓库中提出Issue，我们将尽力为您提供帮助。

## 下载链接

[JDK安装教程Win11环境](https://pan.quark.cn/s/a87d54899c37)