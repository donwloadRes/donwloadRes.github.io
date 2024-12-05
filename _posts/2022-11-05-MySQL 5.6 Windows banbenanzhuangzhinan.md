---
layout: post
title: "MySQL 5.6 Windows 版本安装指南"
date:   2020-04-20
tags: [MySQL,mysql,5.6,安装,Windows]
comments: true
author: admin
---
# MySQL 5.6 Windows 版本安装指南

本资源文件提供了 MySQL 5.6 在 Windows 系统上的安装包及详细的安装步骤。无论你是数据库管理员还是开发者，这份指南都将帮助你顺利完成 MySQL 5.6 的安装。

## 内容概述

- **安装包**：包含 MySQL 5.6 的 Windows 版本安装包。
- **安装步骤**：详细介绍了如何在 Windows 上卸载和安装 MySQL 5.6，包括检查服务、配置环境变量、修改配置文件、安装步骤和设置管理员密码。

## 安装步骤

### 1. 检查本地 MySQL 服务

在安装 MySQL 5.6 之前，首先检查本地是否已经安装了 MySQL 服务。按下 `Win + R`，输入 `services.msc`，查看是否有 MySQL 服务。

### 2. 卸载旧版本 MySQL

如果本地已经安装了 MySQL 服务，需要先停止并卸载旧版本。使用管理员模式打开命令提示符，输入以下命令：

```bash
net stop mysql
mysqld --remove mysql
```

### 3. 解压安装包

将 MySQL 5.6 的安装包解压到你选择的目录中，例如 `D:\mysql-5.6.49-winx64`。

### 4. 配置环境变量

打开系统设置，搜索“环境变量”，找到系统变量中的 `Path` 变量，点击编辑。新建一个变量，将 MySQL 的 `bin` 目录路径添加进去，例如 `D:\mysql-5.6.49-winx64\bin`。

### 5. 修改配置文件

在 MySQL 安装目录中，将 `my-default.ini` 文件复制并重命名为 `my.ini`。打开 `my.ini` 文件，输入以下内容：

```ini
[mysql]
# 设置mysql客户端默认字符集
default-character-set=utf8

[mysqld]
# 设置3306端口
port = 3306
# 设置mysql的安装目录
basedir=D:\mysql-5.6.49-winx64\mysql-5.6.49-winx64
# 设置mysql数据库的数据的存放目录
datadir=D:\mysql-5.6.49-winx64\mysql-5.6.49-winx64\data
# 允许最大连接数
max_connections=200
# 服务端使用的字符集默认为8比特编码的latin1字符集
character-set-server=utf8
# 创建新表时将使用的默认存储引擎
default-storage-engine=INNODB
```

### 6. 安装 MySQL 服务

以管理员身份运行命令提示符，进入 MySQL 的 `bin` 目录，执行以下命令：

```bash
mysqld -install
net start mysql
```

### 7. 登录 MySQL 并设置密码

安装完成后，登录 MySQL 并设置管理员密码：

```bash
mysql -u root -p
```

第一次登录时没有密码，直接按回车。然后执行以下命令设置密码：

```sql
use mysql;
update user set password=password('your_password') where user='root';
flush privileges;
quit;
```

## 注意事项

- 确保在安装过程中使用管理员权限运行命令提示符。
- 在修改配置文件时，确保路径和端口号正确无误。

通过以上步骤，你将成功在 Windows 系统上安装 MySQL 5.6，并设置好管理员密码。

## 下载链接

[MySQL5.6Windows版本安装指南](https://pan.quark.cn/s/edf1f818d987)