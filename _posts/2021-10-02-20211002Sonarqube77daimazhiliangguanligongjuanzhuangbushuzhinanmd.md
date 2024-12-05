---
layout: post
title: "Sonarqube77代码质量管理工具安装部署指南"
date:   2021-12-24
tags: [Sonarqube,安装,7.7,数据库,MySQL]
comments: true
author: admin
---
# Sonarqube-7.7代码质量管理工具安装部署指南

## 概述

本文档提供了详细的指导，帮助您顺利安装与配置Sonarqube 7.7，一个强大的代码质量管理平台。通过Sonarqube，您可以管理源代码质量，支持多种编程语言，如Java、C#、JavaScript等，从多个维度分析代码，确保软件项目的质量和可维护性。

## 准备工作

### 系统需求
- 操作系统：Windows/Linux（示例以CentOS 7为例）
- Java Development Kit (JDK): 1.8版本
- MySQL数据库：建议版本5.6至8.0之间的任意版本

### 主要步骤概览

1. **下载Sonarqube**：从官方网站获取Sonarqube 7.7的安装包。
2. **安装JDK**：确保系统已安装JDK 1.8，并正确配置环境变量。
3. **MySQL数据库安装**：安装并配置MySQL，创建Sonar专用数据库（名为sonar）。
4. **安装VC++通用包**：对于Windows环境，需安装以解决依赖。
5. **Navicat安装（可选）**：用于图形化管理MySQL，便于数据库操作。
6. **配置Sonarqube**：调整Sonarqube的配置文件以指向正确的数据库。
7. **启动Sonarqube服务**：运行启动脚本，保持命令行窗口打开。
8. **访问Web界面**：在浏览器中访问`http://localhost:9000`，开始使用Sonarqube。

## 步骤详解

#### 1. 下载与解压Sonarqube

前往Sonarqube官网下载页面，获取7.7版本的安装包，解压到适当的目录。

#### 2. JDK安装与配置

确保JDK正确安装并添加到PATH环境变量中。

#### 3. MySQL安装与配置

- 安装MySQL 5.6或更高版本。
- 在MySQL中创建名为“sonar”的数据库，不需要手动创建表，Sonarqube会在启动时自动生成所需的表结构。

#### 4. Sonarqube配置

- 编辑`sonarqube-7.7/conf/sonar.properties`文件，配置数据库连接信息，如sonar.jdbc.url应指向刚创建的Sonar数据库。

#### 5. 启动Sonarqube

在Sonarqube安装目录下的`bin`文件夹里，根据操作系统执行对应的启动脚本（如Windows的`StartSonar.bat`）。

#### 6. 验证安装

启动成功后，通过浏览器访问`http://localhost:9000`，如果看到Sonarqube的登录界面，表示安装配置成功。

## 注意事项

- 确保防火墙规则允许9000端口的访问。
- 对于生产环境，考虑使用更细致的配置调整，以及定期备份数据库。

通过上述步骤，您可以成功部署Sonarqube 7.7，开始您的代码质量之旅。

## 下载链接

[Sonarqube-7.7代码质量管理工具安装部署指南](https://pan.quark.cn/s/9aa30c17e177)