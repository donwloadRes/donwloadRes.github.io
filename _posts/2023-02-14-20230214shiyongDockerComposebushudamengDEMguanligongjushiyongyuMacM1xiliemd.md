---
layout: post
title: "使用DockerCompose部署达梦DEM管理工具适用于Mac M1系列"
date:   2023-08-22
tags: [Docker,Compose,DEM,达梦,Mac]
comments: true
author: admin
---
# 使用Docker-Compose部署达梦DEM管理工具（适用于Mac M1系列）

## 简介
本资源文件提供了一个详细的指南，帮助用户在Mac M1系列设备上使用Docker-Compose部署达梦DEM（达梦企业管理工具）。达梦DEM是一个功能强大的Web管理端，集成了达梦数据库的管理工具、数据迁移、性能监视等多种功能。

## 主要内容
1. **环境准备**：
   - 确保已在Mac M1设备上安装Docker和Docker-Compose。
   - 已经搭建好Docker的达梦数据库环境。

2. **部署步骤**：
   - 下载并解压DEM的war包。
   - 修改db.xml文件中的数据库连接地址。
   - 使用Docker-Compose编写并启动服务。

3. **注意事项**：
   - DEM的war包需要手动解压，避免自动解压导致子目录为空的问题。
   - 数据库地址可以直接使用Docker-Compose中的service名称。
   - 确保路径映射正确，避免启动时出现404错误。

## 使用方法
1. 下载本资源文件中的所有内容。
2. 按照指南中的步骤进行操作。
3. 启动Docker-Compose服务后，通过浏览器访问`localhost:8080/dem`，使用默认账号`admin`和密码`888888`登录。

## 其他说明
- 本指南适用于Mac M1系列设备，其他设备可能需要根据实际情况进行调整。
- 如有任何问题，请参考原文档或联系技术支持。

## 贡献
欢迎提交问题和改进建议，帮助我们完善本指南。

## 下载链接

[使用Docker-Compose部署达梦DEM管理工具适用于MacM1系列](https://pan.quark.cn/s/e7ccc7326755)