---
layout: post
title: "JDK 18 下载安装及环境变量配置指南"
date:   2022-01-27
tags: [JDK,点击,1.8,安装,Java]
comments: true
author: admin
---
# JDK 1.8 下载、安装及环境变量配置指南

本资源文件提供了JDK 1.8的下载、安装及环境变量配置的详细步骤。JDK 1.8是Java开发中相对稳定的版本，适用于大多数Java开发项目。以下是具体的操作指南：

## 1. 下载JDK 1.8

### 1.1 百度网盘下载
- **1.8.0_152版本**
  - 提取码：04lf
- **1.8.0_281版本**
  - Windows 64位：提取码：ugg9
  - Windows 32位：提取码：ldm1
- **1.8.0_40版本**
  - 提取码：mrxa

### 1.2 官网下载
- 官网地址：http://www.oracle.com/index.html
- 直接下载地址：Java Downloads | Oracle

## 2. 安装JDK 1.8

### 2.1 安装步骤
1. 双击下载好的JDK安装包，点击“下一步”。
2. 修改JDK默认安装目录（建议不安装在C盘）。
3. 点击“下一步”，修改JRE默认安装目录。
4. 点击“下一步”，进行安装。
5. 点击“关闭”完成安装。

## 3. 配置环境变量

### 3.1 进入环境变量
1. 选择“计算机”，右键选择“属性”。
2. 进入后选择“高级系统设置”，点击“环境变量”。

### 3.2 配置JAVA_HOME
- 在“系统变量”区域，点击“新建”，变量名为JAVA_HOME，变量值为JDK的安装路径（如：D:\Software\Java\jdk1.8.0_331）。

### 3.3 配置CLASSPATH
- 在“系统变量”区域，点击“新建”，变量名为CLASSPATH，变量值为：
  - %JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar

### 3.4 配置Path
- 双击Path进行编辑，点击“新建”，变量值为%JAVA_HOME%\bin，并将它移到第一个，然后点击“确定”。

## 4. 测试JDK是否安装成功

1. 按住键盘上的Win+R，打开运行，输入cmd，点击“确定”进入命令行窗口。
2. 输入`java -version`或`javac -version`获取当前安装的JDK版本信息。
3. 检验`javac.exe`或`javac`命令，检验`java.exe`或`java`命令。

通过以上步骤，您可以成功下载、安装并配置JDK 1.8，确保Java开发环境正常运行。

## 下载链接

[JDK1.8下载安装及环境变量配置指南](https://pan.quark.cn/s/d53e7ab0b71a)