---
layout: post
title: "信息管理系统框架 VS2019  WinForm  SQL Server"
date:   2023-04-11
tags: [管理员,信息,普通用户,SQL,Server]
comments: true
author: admin
---
# 信息管理系统框架 (VS2019 + WinForm + SQL Server)

## 项目简介

本项目提供了一个基于Visual Studio 2019、WinForm和SQL Server的信息管理系统框架。该框架包含了多个模块，支持管理员和普通用户的不同操作需求。特别地，本项目使用了SQL Server数据库，但您也可以使用VS自带的数据库启动，无需安装庞大的SQL Server安装包。

## 主要功能模块

### 管理员模块

1. **管理员登录模块**：管理员通过输入用户名和密码进行登录。
2. **用户管理模块**：管理员可以管理普通用户的账号信息。
3. **信息上传模块**：管理员可以上传信息到系统中。
4. **退出模块**：管理员可以安全退出系统。

### 普通用户模块

1. **用户登录模块**：普通用户通过输入用户名和密码进行登录。
2. **修改信息模块**：普通用户可以修改自己的信息。
3. **信息查询下载模块**：普通用户可以查询信息并将其保存为本地TXT文件。
4. **退出模块**：普通用户可以安全退出系统。

## 数据库设计

本项目使用SQL Server数据库，数据库名称为`OfficeCommonUser`。主要包含以下表：

- **普通用户表 (CommonUser)**：存储普通用户的基本信息。
- **下载信息表 (Download)**：记录用户下载的信息。
- **信息表 (Information)**：存储系统中的信息数据。
- **管理员表 (ManagerUser)**：存储管理员的基本信息。
- **上传信息人员表 (Upload)**：记录管理员上传的信息。

### 表结构

- **普通用户表 (CommonUser)**：
  - `UserID`：用户ID
  - `UserName`：用户名
  - `UserPassword`：用户密码
  - `UserSort`：用户类型

- **下载信息表 (Download)**：
  - `DownloadID`：下载ID
  - `UserID`：用户ID
  - `InformationID`：信息ID
  - `DownloadTime`：下载时间

- **信息表 (Information)**：
  - `InformationID`：信息ID
  - `Title`：信息标题
  - `Content`：信息内容
  - `UploadTime`：上传时间

- **管理员表 (ManagerUser)**：
  - `ManagerID`：管理员ID
  - `ManagerName`：管理员名
  - `ManagerPassword`：管理员密码

- **上传信息人员表 (Upload)**：
  - `UploadID`：上传ID
  - `UploadName`：上传者姓名
  - `UploadTime`：上传时间

## 使用说明

1. **安装Visual Studio 2019**：确保您已安装Visual Studio 2019，并配置好WinForm开发环境。
2. **数据库配置**：您可以选择使用SQL Server数据库，也可以使用VS自带的数据库启动。
3. **运行项目**：打开项目解决方案，编译并运行项目，即可体验信息管理系统的各项功能。

## 注意事项

- 本项目使用SQL Server数据库，但您可以选择使用VS自带的数据库启动，无需安装庞大的SQL Server安装包。
- 请确保在运行项目前，数据库已正确配置并连接。

## 贡献

欢迎大家提出改进建议或提交代码，共同完善这个信息管理系统框架。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[信息管理系统框架VS2019WinFormSQLServer](https://pan.quark.cn/s/250e58b0a5cc)