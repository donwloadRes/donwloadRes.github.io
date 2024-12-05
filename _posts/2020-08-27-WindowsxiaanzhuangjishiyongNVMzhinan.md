---
layout: post
title: "Windows下安装及使用NVM指南"
date:   2021-04-23
tags: [Node,NVM,js,nvm,安装]
comments: true
author: admin
---
# Windows下安装及使用NVM指南

## 简介
本资源文件提供了在Windows系统下安装和使用Node Version Manager（NVM）的详细指南。NVM是一个用于管理多个Node.js版本的工具，它允许用户在同一台机器上轻松切换不同版本的Node.js，以满足不同项目的需求。

## 安装步骤

### 第一步：下载NVM
1. 访问NVM的GitHub仓库，下载最新版本的NVM。
2. 选择并下载`nvm-setup.zip`文件。

### 第二步：安装NVM
1. 解压下载的`nvm-setup.zip`文件。
2. 运行`nvm-setup.exe`，按照安装向导的提示完成安装。

### 第三步：配置环境变量
1. 右键点击“我的电脑”（或“此电脑”）图标，选择“属性”。
2. 点击左侧的“高级系统设置”，然后点击“环境变量”按钮。
3. 在“系统变量”区域找到“Path”变量并编辑它，将NVM的安装路径添加到变量值中（例如：`C:\Users\YourUserName\AppData\Roaming\nvm`）。

### 第四步：安装Node.js
1. 打开命令提示符（或PowerShell），运行以下命令来安装Node.js：
   ```
   nvm install latest
   ```
   这将安装最新版本的Node.js。您还可以使用以下命令来安装特定版本，如：
   ```
   nvm install 14.17.3
   ```

### 第五步：使用Node.js
1. 安装完成后，您可以使用以下命令来切换和使用已安装的Node.js版本：
   ```
   nvm use <version>
   ```
   其中，`<version>`是您要使用的Node.js版本号，例如：
   ```
   nvm use 14.17.3
   ```
2. 您还可以使用以下命令来查看已安装的Node.js版本列表：
   ```
   nvm list
   ```

## 总结
通过以上步骤，您可以在Windows系统上成功安装和使用NVM来管理Node.js版本。NVM的灵活性使得在不同项目中切换Node.js版本变得非常方便，从而提高了开发效率。

## 下载链接

[Windows下安装及使用NVM指南分享](https://pan.quark.cn/s/150ef9e800fb)