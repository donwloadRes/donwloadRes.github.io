---
layout: post
title: "SonarQube 78 安装及使用教程Windows"
date:   2021-12-21
tags: [SonarQube,MySQL,7.8,安装,Windows]
comments: true
author: admin
---
# SonarQube 7.8 安装及使用教程（Windows）

## 简介
本资源文件提供了在Windows环境下安装和使用SonarQube 7.8的详细教程。SonarQube是一个用于管理代码质量的开放平台，能够快速定位代码中潜在的或者明显的错误，支持多种编程语言的代码质量管理与检测。

## 安装步骤
1. **准备工作**
   - 下载SonarQube 7.8安装包。
   - 确保系统已安装JDK 8和MySQL 5.7。

2. **安装MySQL**
   - 解压MySQL安装包。
   - 创建`my.ini`文件并配置MySQL参数。
   - 以管理员身份运行命令提示符，执行MySQL安装和初始化命令。
   - 启动MySQL服务并设置初始密码。

3. **配置SonarQube**
   - 解压SonarQube 7.8安装包。
   - 进入`conf`文件夹，编辑`sonar.properties`文件，配置数据库连接信息。
   - 启动SonarQube服务，访问`localhost:9000`进行配置。

4. **使用SonarQube**
   - 登录SonarQube，默认用户名和密码均为`admin`。
   - 创建项目并进行代码扫描，查看代码质量报告。

## 注意事项
- SonarQube 7.9以后的版本不支持MySQL，建议使用7.8版本。
- 安装过程中需注意MySQL和SonarQube的版本兼容性。

## 参考资料
- 详细安装步骤和配置说明可参考[CSDN博客文章](https://blog.csdn.net/opujioh/article/details/129649853)。

通过本教程，您可以顺利在Windows环境下安装和配置SonarQube 7.8，并开始使用它来提升代码质量。

## 下载链接

[SonarQube7.8安装及使用教程Windows分享](https://pan.quark.cn/s/39a319d2236d)