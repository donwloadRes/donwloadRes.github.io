---
layout: post
title: "MySQL安装与环境变量配置指南"
date:   2021-08-04
tags: [MySQL,mysql,环境变量,安装,点击]
comments: true
author: admin
---
# MySQL安装与环境变量配置指南

本资源文件提供了详细的MySQL安装步骤以及Windows系统下的环境变量配置方法。通过本指南，您可以轻松完成MySQL的安装和配置，确保MySQL在您的系统中正常运行。

## 内容概述

1. **MySQL安装步骤**
   - 下载MySQL压缩包
   - 解压至指定目录
   - 创建配置文件 `my.ini`
   - 通过DOS命令行进行安装
   - 启动MySQL服务
   - 登录MySQL并修改初始密码

2. **环境变量配置**
   - 打开系统属性
   - 进入环境变量设置
   - 新建系统变量 `MYSQL_HOME`
   - 编辑 `Path` 变量，添加MySQL的 `bin` 目录路径

## 安装步骤详解

### 1. 下载MySQL压缩包
从官方网站或其他可信来源下载MySQL的压缩包。

### 2. 解压至指定目录
将下载的压缩包解压至您希望安装MySQL的目录，例如 `D:\Program Files (x86)`。

### 3. 创建配置文件 `my.ini`
在解压后的MySQL目录下创建一个名为 `my.ini` 的文件，并添加以下内容：
```ini
[mysqld]
port=3306
character-set-server=utf8
default-storage-engine=INNODB

[mysql]
default-character-set=utf8

[client]
port=3306
default-character-set=utf8
```

### 4. 通过DOS命令行进行安装
1. 打开命令提示符（以管理员身份运行）。
2. 进入MySQL的 `bin` 目录，例如 `D:\Program Files (x86)\mysql-8.0.25-winx64\bin`。
3. 执行以下命令初始化MySQL：
   ```shell
   mysqld --initialize --user=mysql --console
   ```
4. 安装MySQL服务：
   ```shell
   mysqld --install mysql
   ```

### 5. 启动MySQL服务
在命令提示符中执行以下命令启动MySQL服务：
```shell
net start mysql
```

### 6. 登录MySQL并修改初始密码
1. 执行以下命令登录MySQL：
   ```shell
   mysql -uroot -p
   ```
2. 输入初始密码（在初始化时生成的临时密码）。
3. 修改root用户密码：
   ```sql
   ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '新密码';
   ```

## 环境变量配置

### 1. 打开系统属性
右键点击“此电脑”，选择“属性”，然后点击“高级系统设置”。

### 2. 进入环境变量设置
在“系统属性”窗口中，点击“环境变量”。

### 3. 新建系统变量 `MYSQL_HOME`
在“系统变量”部分，点击“新建”，添加变量名为 `MYSQL_HOME`，变量值为MySQL的安装路径，例如 `D:\Program Files (x86)\mysql-8.0.25-winx64`。

### 4. 编辑 `Path` 变量
在“系统变量”中找到 `Path` 变量，点击“编辑”，然后点击“新建”，添加 `%MYSQL_HOME%\bin`。

## 总结

通过以上步骤，您可以顺利完成MySQL的安装和环境变量的配置。配置完成后，您可以在任意位置通过命令行工具访问MySQL，方便进行数据库的管理和操作。

## 下载链接

[MySQL安装与环境变量配置指南](https://pan.quark.cn/s/d090b9f3a70e)