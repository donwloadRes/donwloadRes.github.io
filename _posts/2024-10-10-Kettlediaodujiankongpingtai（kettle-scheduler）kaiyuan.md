---
layout: post
title: "Kettle调度监控平台（kettle-scheduler）开源"
date:   2021-12-26
tags: [Kettle,监控,kettle,QQ,scheduler]
comments: true
author: admin
---
# Kettle调度监控平台（kettle-scheduler）开源

## 项目介绍
Kettle调度监控平台（以下简称KS）是一个自主开发的Java Web程序，专门用来调度和监控由Kettle客户端创建的Job和Transformation。KS整体的框架是由Spring + Spring MVC + BeetlSQL整合而成，通过调用Kettle的API来执行转换和作业，并且使用Quartz框架完成调度工作。

## 功能特点
1. **调度功能**：支持对Kettle的Job和Transformation进行定时调度。
2. **监控功能**：实时监控Job和Transformation的执行状态，包括成功次数、失败次数等。
3. **日志管理**：记录每次执行的日志，并支持日志下载。
4. **资源库管理**：管理Kettle数据库资源库的信息，支持新增、修改、删除操作。
5. **用户管理**：支持管理用户，包括新增、编辑、删除用户。

## 部署指南
### 基础环境
- 操作系统：Windows（Linux类似）
- 预装软件：JDK 1.8、MySQL、Tomcat、Kettle 8.0

### 部署步骤
1. 将源码中`kettle-scheduler.sql`导入MySQL数据库。
2. 将源码编译打包后解压到Tomcat下的`webapps`目录下。
3. 配置`km\WEB-INF\classes\resource\db.properties`文件，设置MySQL的JDBC连接信息。
4. 配置`km\WEB-INF\classes\resource\kettle.properties`文件，设置Kettle的相关路径和日志级别。
5. 启动Tomcat，访问`http://localhost:8080/km`进入系统。

## 使用说明
1. **登陆**：访问`http://localhost:8080/km`进入登陆界面，用户名`admin`，密码`admin`。
2. **首页**：显示监控信息，包括总监控任务数、监控作业数、监控转换数等。
3. **资源库管理**：管理Kettle数据库资源库的信息。
4. **任务管理**：管理作业和转换的定时任务。
5. **监控管理**：监控作业和转换的执行状态。
6. **用户管理**：管理用户信息。

## 项目源码
项目源码已开源，可在GitHub上获取：[GitHub - zhaxiaodong9860/kettle-scheduler](https://github.com/zhaxiaodong9860/kettle-scheduler)

## 交流与支持
欢迎加入QQ群进行交流和提问：
- QQ群1：817362677（已满）
- QQ群2：821614032（已满）
- QQ群3：553956378（已满）
- QQ群4：881730283

## 贡献与反馈
欢迎大家一起维护此项目，如有问题可加入QQ群提问或提交Issue。

## 下载链接

[Kettle调度监控平台kettle-scheduler开源分享](https://pan.quark.cn/s/1ec58db4236f)