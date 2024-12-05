---
layout: post
title: "JDK 18 环境安装及配置指南"
date:   2024-01-14
tags: [安装,JAVA,JDK,HOME%,1.8]
comments: true
author: admin
---
# JDK 1.8 环境安装及配置指南

本资源文件提供了JDK 1.8在Windows上的安装步骤，包括从Oracle官网下载特定版本、选择安装路径、配置JAVA_HOME、Path和CLASSPATH环境变量，以及如何通过命令行验证安装是否成功。

## 一、下载JDK 1.8

本教程使用的是8u202版本，若需要其他版本可自行前往Oracle官网下载。

## 二、安装

1. 双击下载的安装包，等待安装程序启动。
2. 点击“下一步”，选择安装位置（默认安装在C盘）。
3. 在安装过程中可能会弹出提示框，确认即可。
4. 安装完成后，点击“关闭”。

## 三、环境变量配置

1. 右键点击“此电脑”，选择“属性”。
2. 选择“高级系统设置”。
3. 点击“环境变量”。
4. 新建系统变量：
   - 变量名：JAVA_HOME
   - 变量值：JDK安装目录（例如：C:\Program Files\Java\jdk1.8.0_202）
5. 编辑Path变量，添加以下内容：
   - %JAVA_HOME%\bin
   - %JAVA_HOME%\jre\bin
6. 新建CLASSPATH变量，变量值：
   - %JAVA_HOME%\lib\dt.jar
   - %JAVA_HOME%\lib\tools.jar

## 四、验证

1. 打开命令行（Win+R，输入cmd）。
2. 输入以下命令验证安装是否成功：
   - java
   - javac
   - java -version

通过以上步骤，您可以成功安装并配置JDK 1.8环境。

## 下载链接

[JDK1.8环境安装及配置指南](https://pan.quark.cn/s/7482e25e2746)