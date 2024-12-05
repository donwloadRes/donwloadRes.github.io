---
layout: post
title: "PbootCMS 升级到官网正版及数据库转换为 MySQL 指南"
date:   2020-04-05
tags: [数据库,MySQL,PbootCMS,文件,版本]
comments: true
author: admin
---
# PbootCMS 升级到官网正版及数据库转换为 MySQL 指南

本文详细介绍了如何将 PbootCMS 模板从 SQLite 升级至最新版的 MySQL，包括数据库转换、结构同步以及框架更新步骤，以确保安全性并保持前后端一致性。

## 目录
1. [背景介绍](#背景介绍)
2. [升级步骤](#升级步骤)
   - [第一步：数据库转换](#第一步数据库转换)
   - [第二步：创建并同步新老版本的 MySQL 文件](#第二步创建并同步新老版本的-mysql-文件)
   - [第三步：更新 PbootCMS 框架](#第三步更新-pbootcms-框架)
3. [注意事项](#注意事项)

## 背景介绍
今年下载了一个 PbootCMS 的模板，发现前端不错，但登录后台发现后台框架不是最新的，并且担心有后门文件，因此准备升级到官方最新的版本。

## 升级步骤

### 第一步：数据库转换
1. 下载官方的数据库转换文件。
2. 使用 SQLiteStudio 工具打开 PbootCMS 3.2.3 SQLite 转 MySQL 目录下的 SQLiteStudio.exe 文件。
3. 导入新版本和老版本的数据库。
4. 分别在新老版本数据库上右键，选择导出该数据库。
5. 导出时选择 Next，然后选择导出选项。
6. 打开 PbootCMS 3.2.3 SQLite 转 MySQL 根目录的 pbootcms3.2.3 sqlite 转 mysql.exe 文件。
7. 点击打开文件，选择刚刚导出的数据库文件。
8. 点击生成 MySQL SQL 文件，等待生成完成。

### 第二步：创建并同步新老版本的 MySQL 文件
1. 新建两个 MySQL 数据库，将新老版本数据库分别导入。
2. 下载并安装 Navicat 工具。
3. 链接两个刚刚创建的 MySQL 数据库。
4. 点击工具栏的结构同步。
5. 选择下方如图的两个数据库，然后点击比较。
6. 同步两个数据库的结构。

### 第三步：更新 PbootCMS 框架
1. 保留 config、data、static、template 目录，其余全部用新版替换。
2. 修改 /config/database.php 文件，将数据库改为 MySQL，并对接刚更新完成的老版 MySQL 数据库。

## 注意事项
- 在操作过程中，请确保备份所有重要数据。
- 确保服务器环境满足新版 PbootCMS 的要求。
- 在更新框架后，建议在后台在线更新，再次检测更新下。

通过以上步骤，您可以顺利将 PbootCMS 升级到官网正版，并将数据库转换为 MySQL，确保系统的安全性和一致性。

## 下载链接

[PbootCMS升级到官网正版及数据库转换为MySQL指南](https://pan.quark.cn/s/c13655c05959)