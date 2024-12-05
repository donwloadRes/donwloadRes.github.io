---
layout: post
title: "Ubuntu 2004 下安装 Navicat 120 Premium CS x64"
date:   2020-02-01
tags: [Navicat,x64,navicat,120,Premium]
comments: true
author: admin
---
# Ubuntu 20.04 下安装 Navicat 120 Premium CS x64

本文详细介绍了在 Ubuntu 20.04 操作系统下安装 Navicat 120 Premium CS x64 数据库访问工具的步骤。Navicat 是一款功能强大的数据库管理工具，支持多种数据库，如 MySQL、Oracle、SQL Server 等，能够帮助用户高效地管理和操作数据库。

## 安装步骤

### 1. 下载 Navicat 120 Premium CS x64

首先，从提供的资源文件中下载 Navicat 120 Premium CS x64 安装包。

### 2. 安装 Navicat

将下载的安装包解压到 `/opt` 目录下，然后进入解压后的目录，运行以下命令启动 Navicat：

```bash
tar -zxvf navicat120_premium_cs_x64
cd navicat120_premium_cs_x64
./start_navicat
```

运行后，Navicat 会提示注册并提供14天的试用期。后续将介绍一个快速破解的办法来继续使用该软件。

### 3. 解决乱码问题

在某些情况下，Navicat 启动后可能会出现乱码。解决方法如下：

1. 修改安装目录下的 `start_navicat` 文件中的字符集为 `"zh_CN.UTF-8"`。
2. 如果第一种方法无效，可以通过更改字体的方法解决。在乱码的界面中选择菜单栏第五个选项，将字体改为“中文黑体xxx”。

### 4. 创建快捷方式

为了方便使用，可以为 Navicat 创建桌面快捷方式。执行以下命令：

```bash
cd /usr/share/applications
vi navicat.desktop
```

在 `navicat.desktop` 文件中添加以下内容：

```ini
[Desktop Entry]
Encoding=UTF-8
Name=Navicat
Comment=Navicat12
Exec=/opt/navicat121_mongodb_cs_x64/start_navicat
Icon=/opt/navicat121_mongodb_cs_x64/navicat.png
Terminal=false
StartupNotify=true
Type=Application
Categories=Application;Development
```

### 5. 破解方法

可以通过删除日志文件来不断延长试用期。第一次执行 `start_navicat` 时，会在用户主目录下生成一个名为 `.navicat64` 的隐藏文件夹。删除此文件夹下的 `system.reg`、`user.reg` 和 `userdef.reg` 文件。下次启动 Navicat 时，试用期会重新计算。

## 总结

通过以上步骤，您可以在 Ubuntu 20.04 系统上成功安装并使用 Navicat 120 Premium CS x64 数据库访问工具。希望本文对您有所帮助！

## 下载链接

[Ubuntu20.04下安装Navicat120PremiumCSx64分享](https://pan.quark.cn/s/76cc4fc8a399)