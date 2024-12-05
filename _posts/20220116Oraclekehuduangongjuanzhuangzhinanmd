---
layout: post
title: "Oracle客户端工具安装指南"
date:   2020-03-27
tags: [点击,instantclient,Oracle,客户端,安装]
comments: true
author: admin
---
# Oracle客户端工具安装指南

本仓库提供了一个资源文件，用于安装Oracle客户端工具，包括PL/SQL Developer和instantclient。以下是详细的安装步骤和配置说明。

## 资源文件内容

- **PL/SQL Developer**: 一个用于Oracle数据库开发的图形界面工具。
- **instantclient**: Oracle提供的轻量级数据库客户端，无需安装标准客户端即可运行OCI、OCCI、Pro*C、ODBC和JDBC程序。

## 安装步骤

### 1. PL/SQL Developer安装

1. 双击`plsqldev134x32.msi`文件，进入安装页面，点击`Next`。
2. 选择“I accept the terms in the license agreement”，点击`Next`。
3. 修改安装地址，选择“Enter license information”直接进入激活版，点击`Next`。
4. 根据`PLSQL Developer注册.txt`文件输入信息，点击`Next`。
5. 默认选项，点击`Next`。
6. 点击`Install`，稍等20秒，安装成功。
7. 查看PL/SQL工具的年限。

### 2. 设置PL/SQL Developer为中文版

1. 在同目录下双击`chinese.exe`文件，点击【确定】。
2. 点击下一步，直至完成。
3. 重启软件，验证设置中文版是否成功。
4. 如果重启软件后还是英文，汉化不成功的话，直接修改首选项的配置。

### 3. instantclient客户端配置

1. 在`instantclient_12_1`文件夹下创建`network/admin/tnsnames.ora`文件。
2. 配置环境变量：
   - 右击“我的电脑” - “属性” - “高级系统设置” - “环境变量”。
   - 点击“新建”，新建变量：
     - 变量名：`NLS_LANG`
     - 变量值：`SIMPLIFIED CHINESE_CHINA.ZHS16GBK`
   - 点击【新建】，新建变量：
     - 变量名：`ORACLE_HOME`
     - 变量值：`D:\wokespace\tools\instantclient_12_1`（instantclient文件路径）
   - 点击【新建】，新建变量：
     - 变量名：`TNS_ADMIN`
     - 变量值：`D:\wokespace\tools\instantclient_12_1\network\admin`（tnsnames.ora文件所在的目录下）
   - 在`path`变量中，添加`%ORACLE_HOME%`。

## 注意事项

- 本仓库提供的PL/SQL Developer和instantclient客户端均为32位版本。
- 如果需要安装64位版本，请自行上网查找相关资源。

## 常见问题

- 如果在配置环境变量后，PLSQL Developer仍然无法连接Oracle数据库，请检查环境变量配置是否正确。
- 如果汉化不成功，请检查首选项配置是否正确。

## 联系我们

如果在安装过程中遇到任何问题，欢迎联系我们获取帮助。

## 下载链接

[Oracle客户端工具安装指南](https://pan.quark.cn/s/ca73e9b71728)