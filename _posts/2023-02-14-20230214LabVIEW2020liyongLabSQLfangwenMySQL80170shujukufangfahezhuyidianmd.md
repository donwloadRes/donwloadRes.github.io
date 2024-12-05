---
layout: post
title: "LabVIEW2020 利用LabSQL访问MySQL8.0.17.0数据库方法和注意点"
date:   2023-10-05
tags: [ODBC,32,LabVIEW2020,数据源,64]
comments: true
author: admin
---
# LabVIEW2020 利用LabSQL访问MySQL8.0.17.0数据库方法和注意点

本文详细记录了在Win10 64位系统上，使用32位LabVIEW2020通过LabSQL工具包连接64位MySQL8.0数据库的过程。关键点包括：安装32位ODBC Connector，配置32位ODBC数据源，确保所有组件与LabVIEW版本兼容。

## 一、需要软件

1. **MySQL 数据库软件**（64位）
2. **ODBC Connecter 软件**（32位）
3. **Navicat for MySQL**
4. **LabSQL工具包**

### 1. MySQL的安装过程
可以参考相关博客，按照步骤进行安装。

### 2. Navicat for MySQL
参见百度网盘，提取码为520y。

### 3. LabSQL工具包
下载后放到LabVIEW软件安装文件下C:\Program Files (x86)\National Instruments\LabVIEW 2020\user\lib下即可。

## 二、配置步骤

1. **安装32位ODBC Connector**
   由于LabVIEW2020是32位，因此必须安装32位的ODBC Connecter软件。

2. **配置32位ODBC数据源**
   确保在32位的ODBC数据源管理程序中配置，不能在64位的ODBC数据源管理程序中配置。

3. **确保所有组件兼容**
   确保LabVIEW2020、MySQL数据库、ODBC Connecter和ODBC数据源之间的版本兼容性。

## 三、注意事项

1. **MySQL 8.0是64位数据库**，安装后会默认安装64位的ODBC Connecter软件，需单独下载安装32位的ODBC Connecter软件。
2. **LabVIEW2020是32位**，因此ODBC Connecter软件和ODBC数据源都必须配置为32位。

## 四、致谢

感谢所有提供相关教程和资源的博主和开发者，帮助我们顺利完成LabVIEW2020与MySQL8.0的连接。

## 下载链接

[LabVIEW2020利用LabSQL访问MySQL8.0.17.0数据库方法和注意点分享](https://pan.quark.cn/s/59957646a368)