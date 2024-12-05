---
layout: post
title: "AJReport 初学入门教程"
date:   2023-06-11
tags: [AJ,Report,配置,MySQL,大屏]
comments: true
author: admin
---
# AJ-Report 初学(入门教程)

## 简介
AJ-Report 是一个完全开源的 BI 平台，专注于酷炫大屏展示，能够随时随地掌控业务动态，让每个决策都有数据支撑。它支持多数据源，内置 MySQL、Elasticsearch、Kudu 等多种驱动，支持自定义数据集，省去数据接口开发。目前已支持 20 种大屏组件/图表，即使不会开发，照着设计稿也可以制作大屏。三步轻松完成大屏设计：配置数据源 → 写 SQL 配置数据集 → 拖拽配置大屏 → 保存发布。

## 下载
本仓库提供了 AJ-Report 的入门教程资源文件，帮助初学者快速上手。资源文件包括 AJ-Report 的发行版和源码，以及相关的配置和启动说明。

## 环境准备
在开始使用 AJ-Report 之前，请确保您的开发环境满足以下要求：
- MySQL 5.7 或更高版本
- Node.js 版本不超过 v16
- JDK 1.8 或更高版本

## 发行版的配置与启动
1. 修改 `bootstrap.yml` 文件中的数据库配置，将其指向您本地的 MySQL 数据库。
2. 修改 `start.bat` 文件，配置您的 JDK 路径。
3. 双击 `start.bat` 文件启动 AJ-Report。

## 源码的配置与启动
1. 使用 IDEA 导入项目，其中 `report-core` 是后端代码，`report-ui` 是前端代码。
2. 配置 `bootstrap.yml` 文件中的数据库连接信息。
3. 启动后端服务。
4. 在前端目录下执行 `npm install` 安装依赖，然后执行 `npm run dev` 启动前端。

## 常见问题
- **后端启动失败**：检查 MySQL 版本和配置是否正确。
- **前端 npm install 失败**：确保 Node.js 版本不超过 v16，并使用淘宝镜像源。
- **请求超时问题**：调整前端设置的请求超时时间。
- **空值导致的空指针异常**：在 SQL 语句中对空值进行处理。

## 总结
通过本教程，您可以快速了解 AJ-Report 的基本使用方法，并能够配置和启动 AJ-Report 进行大屏展示。希望本资源文件对您的学习有所帮助。

## 下载链接

[AJ-Report初学入门教程](https://pan.quark.cn/s/d3e6c58d5d60)