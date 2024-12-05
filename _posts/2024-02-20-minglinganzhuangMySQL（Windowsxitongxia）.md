---
layout: post
title: "命令安装MySQL（Windows系统下）"
date:   2023-11-06
tags: [MySQL,安装,mysql,解压,Windows]
comments: true
author: admin
---
# 命令安装MySQL（Windows系统下）

本仓库提供了一个资源文件，详细介绍了如何在Windows系统下通过命令行安装MySQL。以下是安装步骤的简要概述：

## 安装步骤

1. **下载MySQL安装文件**：
   - 访问MySQL官方网站，找到并下载MySQL Community Server 5.7版本。
   - 选择与电脑位数对应的版本，下载ZIP Archive文件。

2. **解压安装文件**：
   - 将下载的ZIP文件解压到任意目录，建议解压目录不要包含中文。

3. **配置MySQL环境变量**：
   - 右键点击“此电脑” -> 属性 -> 高级系统设置 -> 环境变量。
   - 在系统变量中新建一个变量，变量名为`MYSQL_HOME`，变量值为MySQL解压后的目录。
   - 在系统变量`Path`中添加`%MYSQL_HOME%\bin`。

4. **新建my.ini文件**：
   - 使用文本编辑器（如Sublime或Notepad++）新建一个`my.ini`文件，并将其保存在MySQL解压目录下。
   - 文件内容如下：
     ```ini
     [mysqld]
     port=3306
     character_set_server=utf8
     basedir=D:/soft/Mysql/mysql-5.7.24-winx64/
     datadir=D:/soft/Mysql/mysql-5.7.24-winx64/data
     sql_mode=NO_ENGINE_SUBSTITUTION,STRICT_TRANS_TABLES
     [WinMySQLAdmin]
     D:/soft/Mysql/mysql-5.7.24-winx64/bin/mysqld.exe
     ```

5. **安装MySQL**：
   - 以管理员身份打开Windows PowerShell。
   - 输入以下命令安装MySQL：
     ```bash
     mysqld -install
     ```
   - 初始化MySQL：
     ```bash
     mysqld --initialize
     ```

6. **启动MySQL服务**：
   - 输入以下命令启动MySQL服务：
     ```bash
     net start mysql
     ```

7. **修改MySQL密码**：
   - 进入MySQL命令行：
     ```bash
     mysql -uroot -p
     ```
   - 输入初始化时生成的随机密码，进入MySQL命令行后，修改密码：
     ```sql
     SET PASSWORD = PASSWORD('新密码');
     ALTER USER 'root'@'localhost' PASSWORD EXPIRE NEVER;
     flush privileges;
     ```

## 注意事项
- 确保在安装过程中使用管理员权限运行命令行工具。
- 安装过程中生成的随机密码需要妥善保存，以便后续登录使用。

通过以上步骤，您可以在Windows系统下成功安装并配置MySQL。

## 下载链接

[命令安装MySQLWindows系统下](https://pan.quark.cn/s/e337f52ac444)