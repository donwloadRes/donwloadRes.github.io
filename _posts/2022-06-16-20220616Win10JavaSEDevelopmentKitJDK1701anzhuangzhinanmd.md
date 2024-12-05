---
layout: post
title: "Win10 Java SE Development Kit JDK 1701 安装指南"
date:   2021-08-31
tags: [JDK,安装,Java,点击,17.0]
comments: true
author: admin
---
# Win10 Java SE Development Kit (JDK) 17.0.1 安装指南

本仓库提供了一个资源文件，用于在Windows 10系统上安装Java SE Development Kit (JDK) 17.0.1。JDK是Java开发的核心工具包，包含了Java编译器、运行时环境、开发工具和基础类库等。

## 安装步骤

### 1. 下载JDK安装包

从本仓库下载JDK 17.0.1的安装包。下载完成后，打开文件进行安装。

### 2. 安装JDK

1. 打开下载的安装包，点击“下一步”开始安装。
2. 更改安装路径（建议不要安装在C盘，同时文件夹名字最好是英文，不要带中文）。
3. 点击“下一步”，等待安装完成。

### 3. 配置环境变量

1. 右键点击“此电脑”或“计算机”，选择“属性”。
2. 点击“高级系统设置”。
3. 在“高级”选项卡下，点击“环境变量”。
4. 在“系统变量”中，新建一个变量：
   - 变量名：`JAVA_HOME`
   - 变量值：JDK的安装路径（例如：`C:\Java\jdk-17.0.1`）
5. 在“系统变量”中找到`Path`，点击“编辑”，新建两个变量：
   - `%JAVA_HOME%\bin`
   - `%JAVA_HOME%\jre\bin`
6. 点击“确定”保存所有更改。

### 4. 验证安装

1. 按下`Win + R`键，输入`cmd`，打开命令提示符。
2. 输入以下命令验证JDK是否安装成功：
   - `java -version`
   - `javac -version`
   - `java`
   - `javac`

如果命令执行后显示相应的版本信息，说明JDK安装成功。

## 注意事项

- 安装路径很重要，建议截图记录下来，后续配置环境变量时会用到。
- 配置环境变量时，标点符号一定要在英文输入状态下进行输入，不能是中文状态下的。

通过以上步骤，您可以在Windows 10系统上成功安装并配置JDK 17.0.1，开始您的Java开发之旅。

## 下载链接

[Win10JavaSEDevelopmentKitJDK17.0.1安装指南](https://pan.quark.cn/s/18a0f3d97161)