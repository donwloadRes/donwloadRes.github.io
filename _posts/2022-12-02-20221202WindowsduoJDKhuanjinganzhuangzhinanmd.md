---
layout: post
title: "Windows多JDK环境安装指南"
date:   2024-08-21
tags: [JDK,JAVA,安装,变量,17]
comments: true
author: admin
---
# Windows多JDK环境安装指南

本资源文件提供了在Windows系统上安装多个JDK环境（包括JDK 6、JDK 8和JDK 17）的详细步骤。通过本指南，您可以轻松地在同一台机器上配置和管理多个JDK版本，以满足不同项目的需求。

## 内容概述

1. **JDK 8安装步骤**
   - 下载JDK 8
   - 安装JDK 8
   - 配置环境变量
   - 指定使用的JDK版本
   - 测试安装

2. **JDK 17安装步骤**
   - 下载JDK 17
   - 安装JDK 17
   - 配置环境变量
   - 指定使用的JDK版本
   - 测试安装

## 安装步骤详解

### 1. JDK 8安装

#### 1.1 下载JDK 8
- 从Oracle官网下载JDK 8安装包。

#### 1.2 安装JDK 8
- 创建两个目录（分别存放JDK和JRE）。
- 双击安装包，选择JDK和JRE的安装目录。
- 等待安装完成。

#### 1.3 配置环境变量
- 在系统变量中新建一个名为`JAVA_HOME8`的变量，变量值为JDK 8的安装路径。
- 在系统变量中新建一个`CLASSPATH`变量，变量值为`%JAVA_HOME8%\lib\dt.jar;%JAVA_HOME8%\lib\tools.jar;%JAVA_HOME8%\lib`。
- 在`Path`变量中添加`%JAVA_HOME8%\bin`，并将其上移到最上方。

#### 1.4 指定使用的JDK版本
- 在系统变量中新建一个名为`JAVA_HOME`的变量，变量值为`%JAVA_HOME8%`。

#### 1.5 测试安装
- 打开命令提示符，输入`java -version`，确认JDK 8已成功安装。

### 2. JDK 17安装

#### 2.1 下载JDK 17
- 从Oracle官网下载JDK 17安装包。

#### 2.2 安装JDK 17
- 创建安装目录。
- 双击安装包，选择JDK的安装目录。
- 等待安装完成。

#### 2.3 配置环境变量
- 在系统变量中新建一个名为`JAVA_HOME17`的变量，变量值为JDK 17的安装路径。
- 在系统变量中新建一个`CLASSPATH`变量，变量值为`%JAVA_HOME17%\lib\dt.jar;%JAVA_HOME17%\lib\tools.jar;%JAVA_HOME17%\lib`。
- 在`Path`变量中添加`%JAVA_HOME17%\bin`，并将其上移到最上方。

#### 2.4 指定使用的JDK版本
- 在系统变量中新建一个名为`JAVA_HOME`的变量，变量值为`%JAVA_HOME17%`。

#### 2.5 测试安装
- 打开命令提示符，输入`java -version`，确认JDK 17已成功安装。

## 注意事项

- 在切换JDK版本时，只需修改`JAVA_HOME`变量的值即可。
- 确保每次修改环境变量后，重新打开命令提示符以使更改生效。

通过本指南，您可以轻松地在Windows系统上安装和管理多个JDK版本，满足不同项目的需求。

## 下载链接

[Windows多JDK环境安装指南](https://pan.quark.cn/s/550842b53f61)