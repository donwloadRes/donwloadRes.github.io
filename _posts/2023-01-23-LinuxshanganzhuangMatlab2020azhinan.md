---
layout: post
title: "Linux上安装Matlab2020a指南"
date:   2023-08-03
tags: [Matlab,sudo,matlab,安装,Linux]
comments: true
author: admin
---
# Linux上安装Matlab2020a指南

本仓库提供了一个详细的指南，帮助你在Linux系统上安装Matlab 2020a。以下是安装步骤的简要概述：

## 安装步骤

### 1. 下载“Crack”和“ISO”镜像文件
首先，你需要下载Matlab 2020a的“Crack”和“ISO”镜像文件。你可以通过提供的链接下载这些文件。

### 2. 安装MATLAB
#### 2.1 挂载镜像并开始运行install文件
在终端中执行以下命令：
```bash
cd ~
sudo mkdir matlab
cd matlab
sudo mount -t auto -o loop Matlab98R2020a_Lin64.iso
sudo ./install
```

#### 2.2 选择“使用Key安装”
在安装过程中，选择“使用Key安装”选项，并输入以下安装Key：
```
09806-07443-53955-64350-21751-41297
```

#### 2.3 取消挂载
安装完成后，取消挂载镜像文件：
```bash
sudo umount matlab/
```

### 3. 激活MATLAB
将“Crack”文件夹中的`libmwlmgrimpl.so`文件复制到以下目录：
```bash
sudo cp Linux_Patch/Mathworks\ Matlab\ R2020a\ Linux\ x64\ Crack/libmwlmgrimpl.so /applications/Polyspace/r2020a/bin/glnxa/matlab_startup_plugins/lmgrimpl
```

### 4. 创建快捷启动方式
你可以通过以下方法创建一个快捷启动方式，以便更方便地启动Matlab：

#### 方法一：创建桌面文件
```bash
sudo vim /usr/share/applications/Matlab2020a.desktop
```
输入以下内容：
```
[Desktop Entry]
Categories=Development;Matlab;
Comment[zh_CN]=Matlab: The Language of Technical Computing
Comment=Matlab: The Language of Technical Computing
Exec=sh /usr/local/MATLAB/R2020a/bin/matlab -desktop
GenericName[zh_CN]=Matlab2020a
GenericName=Matlab2020a
Icon=/usr/local/MATLAB/R2020a/toolbox/sl3d/mainpage/matlab_logo.gif
Mimetype=
Name[zh_CN]=MATLAB
Name=MATLAB
Path=
StartupNotify=true
Terminal=false
Type=Application
```

#### 方法二：通过命令行安装小插件
在终端输入：
```bash
sudo apt-get install matlab-support
```
根据提示输入Matlab的bin文件夹目录。

## 注意事项
- 在安装过程中，如果遇到挂载问题，可以尝试编辑`/etc/fstab`文件，添加挂载信息。
- 安装完成后，记得取消挂载并删除`/etc/fstab`中添加的挂载信息，以避免重启后无法进入图形界面。

通过以上步骤，你应该能够在Linux系统上成功安装并激活Matlab 2020a。

## 下载链接

[Linux上安装Matlab2020a指南](https://pan.quark.cn/s/36cca8d895e3)