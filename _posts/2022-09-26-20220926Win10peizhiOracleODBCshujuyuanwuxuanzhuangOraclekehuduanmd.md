---
layout: post
title: "Win10配置Oracle ODBC数据源无需安装Oracle客户端"
date:   2022-04-24
tags: [Oracle,数据源,ODBC,instantclient,windows]
comments: true
author: admin
---
# Win10配置Oracle ODBC数据源（无需安装Oracle客户端）

## 简介

本仓库提供了一个资源文件的下载，帮助用户在Windows 10系统中配置Oracle ODBC数据源，而无需安装Oracle客户端。通过本资源文件，用户可以轻松实现与Oracle数据库的连接，适用于需要快速配置ODBC数据源的开发者和管理员。

## 资源文件内容

- **base包**：instantclient-basic-windows.x64-12.1.0.2.0.zip
- **ODBC包**：instantclient-odbc-windows.x64-12.1.0.2.0.zip

## 使用步骤

### 1. 下载驱动包

下载本仓库提供的两个驱动包：
- `instantclient-basic-windows.x64-12.1.0.2.0.zip`
- `instantclient-odbc-windows.x64-12.1.0.2.0.zip`

### 2. 解压安装

将两个解压包中的文件放到同一个目录，例如`D:\Oracle\instantclient_12_1`。使用管理员权限打开CMD，进入该目录并运行`odbc_install.exe`。执行成功后，终端会出现`Oracle ODBC Driver is installed successfully`信息。

### 3. 设置环境变量

鼠标右键点击“计算机” > “属性” > “高级系统设置” > “高级” > “环境变量” > “系统变量”，添加以下变量：

- `ORACLE_HOME`：`D:\Oracle\instantclient_12_1`
- `Path`：`%ORACLE_HOME%`
- `TNS_ADMIN`：`%ORACLE_HOME%\network\ADMIN`

注意：如果驱动包中没有`network\ADMIN`目录，则需要新建该目录，并在`ADMIN`目录下添加`tnsnames.ora`文件，内容如下：

```
XE =
(DESCRIPTION =
  (ADDRESS = (PROTOCOL = TCP)(HOST = 192.168.0.1)(PORT = 1527))
  (CONNECT_DATA =
    (SERVER = DEDICATED)
    (SERVICE_NAME = XE)
  )
)
```

### 4. 配置ODBC

打开ODBC驱动器，路径为：“开始” > “控制面板” > “管理工具” > “ODBC数据源(64位)”。设置数据源：

- **Data Source Name**：自定义名称，如“Oracle”
- **Description**：连接描述
- **TNS Service Name**：选择`tnsnames.ora`中配置的名称，如“XE”
- **UserID**：访问数据库的用户名

点击“Test Connection”进行连接测试，输入密码后点击“OK”。若连接成功，则提示“Connection successful”。

## 注意事项

- 确保操作系统位数与驱动包位数一致（32位或64位）。
- 配置环境变量时，路径需根据实际解压路径进行调整。

通过以上步骤，您可以在Windows 10系统中成功配置Oracle ODBC数据源，无需安装Oracle客户端，实现与Oracle数据库的快速连接。

## 下载链接

[Win10配置OracleODBC数据源无需安装Oracle客户端分享](https://pan.quark.cn/s/e3f55abe5807)