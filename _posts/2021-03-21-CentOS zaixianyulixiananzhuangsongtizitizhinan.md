---
layout: post
title: "CentOS 在线与离线安装宋体字体指南"
date:   2020-04-13
tags: [ttmkfdir,字体,fonts,bash,安装]
comments: true
author: admin
---
# CentOS 在线与离线安装宋体字体指南

本资源文件提供了在CentOS系统中在线和离线安装宋体字体的详细步骤。无论您是否有网络连接，都可以通过本指南成功安装宋体字体。

## 内容概述

### 一、安装方式

1. **在线安装**
   - 安装字体库
   - 安装ttmkfdir
   - 执行ttmkfdir命令

2. **离线安装**
   - 下载安装文件
   - 安装
   - 执行ttmkfdir命令

### 二、配置

1. 上传字体
2. 添加文件夹权限
3. 编辑配置文件
4. 刷新内存中的字体缓存

## 详细步骤

### 在线安装

1. **安装字体库**
   ```bash
   yum -y install fontconfig
   ```
   安装完成后，在`/usr/shared`目录下会看到`fonts`和`fontconfig`目录。

2. **安装ttmkfdir**
   ```bash
   yum -y install ttmkfdir
   ```
   ttmkfdir用于搜索目录中所有的字体信息，并汇总生成`fonts.scale`文件。

3. **执行ttmkfdir命令**
   ```bash
   ttmkfdir -e /usr/share/X11/fonts/encodings/encodings.dir
   ```

### 离线安装

1. **下载安装文件**
   下载以下两个RPM包：
   - `fontconfig-2.13.0-4.3.el7.x86_64.rpm`
   - `ttmkfdir-3.0.9-42.el7.x86_64.rpm`

2. **安装**
   ```bash
   rpm -ivh fontconfig-2.13.0-4.3.el7.x86_64.rpm --nodeps --force
   rpm -ivh ttmkfdir-3.0.9-42.el7.x86_64.rpm --nodeps --force
   ```

3. **执行ttmkfdir命令**
   ```bash
   ttmkfdir -e /usr/share/X11/fonts/encodings/encodings.dir
   ```

### 配置

1. **上传字体**
   将需要的字体包上传到服务器某一个文件夹，例如`/usr/share/fonts/chinese`。

2. **添加文件夹权限**
   ```bash
   chmod -R 755 /usr/share/fonts/chinese
   ```

3. **编辑配置文件**
   编辑`/etc/fonts/fonts.conf`文件，添加字体文件路径：
   ```xml
   <dir>/usr/share/fonts/chinese</dir>
   ```

4. **刷新内存中的字体缓存**
   ```bash
   fc-cache
   ```

5. **查看字体列表**
   ```bash
   fc-list
   ```
   确认宋体字体包含在其中。

通过以上步骤，您可以在CentOS系统中成功安装宋体字体，并确保系统能够正确识别和使用该字体。

## 下载链接

[CentOS在线与离线安装宋体字体指南](https://pan.quark.cn/s/5e395ec1a3fb)