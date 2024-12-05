---
layout: post
title: "东方通TongWeb外置容器部署Spring Boot项目指南"
date:   2024-10-13
tags: [TongWeb,war,Spring,Boot,部署]
comments: true
author: admin
---
# 东方通TongWeb外置容器部署Spring Boot项目指南

本文档详细介绍了如何在东方通TongWeb（外置容器）中部署Spring Boot项目，并将项目的打包方式从jar包改为war包。通过本指南，您可以轻松地将Spring Boot项目迁移到东方通TongWeb环境中，并确保项目的顺利运行。

## 内容概述

1. **准备工作**
   - 将Spring Boot项目打包方式从jar包改为war包。
   - 排除内置Tomcat依赖。
   - 修改启动类以适应外置容器。

2. **东方通TongWeb安装与配置**
   - 下载并安装东方通TongWeb。
   - 配置TongWeb自启动。
   - 启动和停止TongWeb服务。
   - 访问TongWeb控制台。

3. **配置虚拟主机及HTTP通道**
   - 创建虚拟主机。
   - 配置HTTP通道。

4. **部署前后端应用（war包）**
   - 单独部署前端应用。
   - 部署后端应用。

## 详细步骤

### 1. 准备工作

#### 1.1 修改打包方式
将Spring Boot项目的打包方式从jar包改为war包，具体步骤如下：
- 修改pom.xml文件，将打包方式更改为war。
- 排除内置Tomcat依赖。

#### 1.2 修改启动类
启动类需要继承`SpringBootServletInitializer`类，并重写`configure`方法。

### 2. 东方通TongWeb安装与配置

#### 2.1 下载与安装
从官方渠道下载东方通TongWeb安装包，并按照官方文档进行安装。

#### 2.2 配置自启动
配置TongWeb自启动，确保服务在系统启动时自动运行。

#### 2.3 启动与停止服务
通过命令行启动和停止TongWeb服务。

#### 2.4 访问控制台
使用默认账号和密码访问TongWeb控制台，进行进一步的配置和管理。

### 3. 配置虚拟主机及HTTP通道

#### 3.1 创建虚拟主机
在TongWeb控制台中创建虚拟主机，配置主机名称和别名。

#### 3.2 配置HTTP通道
配置HTTP通道，类似于Nginx的代理配置，确保前后端应用的正常访问。

### 4. 部署前后端应用（war包）

#### 4.1 单独部署前端
将前端应用打包为war包，并上传至TongWeb进行部署。

#### 4.2 部署后端应用
将后端应用打包为war包，并上传至TongWeb进行部署。

## 总结

通过本指南，您可以顺利地将Spring Boot项目部署到东方通TongWeb环境中，并确保项目的正常运行。如果在部署过程中遇到任何问题，请参考东方通TongWeb的官方文档或联系技术支持。

## 下载链接

[东方通TongWeb外置容器部署SpringBoot项目指南](https://pan.quark.cn/s/5be2444b0784)