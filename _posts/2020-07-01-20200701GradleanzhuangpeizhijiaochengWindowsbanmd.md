---
layout: post
title: "Gradle安装配置教程Windows版"
date:   2023-08-05
tags: [Gradle,JDK,下载,安装,配置]
comments: true
author: admin
---
# Gradle安装配置教程（Windows版）

本教程详细介绍了如何在Windows操作系统上安装和配置Gradle。Gradle是一个基于JVM的构建工具，广泛用于Java项目的构建和管理。通过本教程，您将学会如何检查与安装JDK、下载Gradle、配置Gradle环境变量，并通过修改下载源提高效率。此外，本教程还指导您如何在IntelliJ IDEA和Eclipse中创建Gradle项目，添加JUnit测试依赖，并执行测试用例。

## 一、安装前检查

1. **检查JDK安装**：
   - 如果电脑上未安装JDK，请先安装JDK。推荐使用JDK 8及以上版本。
   - 已安装JDK的用户，按Win和R键，输入cmd，然后点击确定。
   - 输入`java -version`，按回车键，查看JDK安装信息。如果有版本信息提示，说明JDK安装成功。

## 二、Gradle下载

1. **选择下载方式**：
   - 方式一：百度网盘下载（提供备用下载链接）。
   - 方式二：官网下载（推荐）。
     - 打开官网下载界面：https://gradle.org/releases/
     - 选择合适的版本下载，推荐使用6.8及以上版本。

## 三、Gradle配置环境变量

1. **解压安装包**：
   - 将下载的压缩包解压到指定目录，建议解压目录只包含英文路径。

2. **配置环境变量**：
   - 在系统变量中新建变量`GRADLE_HOME`，变量值为解压目录路径。
   - 在系统变量`Path`中添加`%GRADLE_HOME%\bin`。

3. **验证安装**：
   - 打开命令提示行，输入`gradle -v`，如果有版本信息提示，说明Gradle环境变量配置成功。

## 四、配置下载源

1. **修改下载源**：
   - 由于Gradle自带Maven下载源是国外的，下载依赖较慢，建议将下载源换成国内镜像。
   - 在Gradle目录下的`init.d`文件夹中新建`init.gradle`文件，添加国内镜像配置。

## 五、IntelliJ IDEA创建Gradle项目

1. **新建Gradle项目或模块**。
2. **配置Gradle**：
   - 按`Ctrl + Alt + S`打开设置，找到Gradle并按提示设置。
3. **添加JUnit依赖**：
   - 在`build.gradle`文件中添加`testImplementation 'junit:junit:4.12'`依赖。
4. **创建测试类并运行**。

## 六、Eclipse创建Gradle项目

1. **配置Eclipse**：
   - 打开`Windows --> Preferences`，按提示配置。
2. **新建Gradle项目**。
3. **添加JUnit依赖**：
   - 在`build.gradle`文件中添加`testImplementation 'junit:junit:4.12'`依赖。
4. **创建测试类并运行**。

通过本教程，您将能够顺利在Windows系统上安装和配置Gradle，并在主流IDE中创建和管理Gradle项目。

## 下载链接

[Gradle安装配置教程Windows版](https://pan.quark.cn/s/995659c8a7b0)