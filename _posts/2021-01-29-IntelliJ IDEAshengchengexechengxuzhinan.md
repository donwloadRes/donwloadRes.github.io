---
layout: post
title: "IntelliJ IDEA生成exe程序指南"
date:   2022-09-26
tags: [exe,Java,JAR,launch,生成]
comments: true
author: admin
---
# IntelliJ IDEA生成exe程序指南

本资源文件详细介绍了如何使用IntelliJ IDEA将Java项目打包成可执行的exe文件。通过本指南，您可以轻松地将编写的Java程序转换为exe格式，使其能够在没有Java环境的电脑上运行。

## 主要步骤

1. **生成JAR包**
   - 打开IntelliJ IDEA，选择`File` -> `Project Structure`。
   - 点击`Artifacts`按钮，添加一个新的Artifact。
   - 配置Artifact的路径和主类，确保勾选`Build on make`。
   - 点击`Build` -> `make Project`，生成JAR包。

2. **准备exe生成工具**
   - 下载并解压`launch.exe`工具包（解压密码为`onepoint`）。
   - 创建一个新的文件夹，将生成的JAR包和JDK中的`jre`目录复制到该文件夹中。

3. **配置exe文件**
   - 将`launch.exe`和`launcher.cfg`文件复制到新建的文件夹中。
   - 使用记事本打开`launcher.cfg`，配置JAR包和JRE的路径。
   - 双击`launch.exe`运行Java应用程序。

4. **自定义图标**
   - 使用`Resource Hacker`工具替换`launch.exe`的图标。
   - 保存修改后的exe文件，并测试运行。

通过以上步骤，您可以将Java项目成功打包成exe文件，并在其他电脑上运行。

## 下载链接

[IntelliJIDEA生成exe程序指南分享](https://pan.quark.cn/s/78d409e4c968)