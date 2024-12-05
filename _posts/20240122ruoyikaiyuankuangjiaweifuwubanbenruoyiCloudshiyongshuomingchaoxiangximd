---
layout: post
title: "若依开源框架-微服务版本（ruoyi-Cloud）使用说明-超详细"
date:   2023-07-22
tags: [Nacos,ruoyi,Cloud,启动,开源]
comments: true
author: admin
---
# 若依开源框架-微服务版本（ruoyi-Cloud）使用说明-超详细

## 简介
本资源文件提供了若依开源框架微服务版本（ruoyi-Cloud）的详细使用说明。若依开源框架是一个基于Spring Boot和Spring Cloud的企业级快速开发平台，适用于构建微服务架构的后台管理系统。

## 环境准备
在开始使用之前，请确保您的开发环境满足以下要求：
- JDK 1.8
- MySQL 5.7及以上
- Nacos 2.0.3
- Node 14版本及以上

## 下载与安装
1. **下载**：访问若依官方网站，点击下载ruoyi-Cloud项目。
2. **解压**：将下载的项目解压到您的开发目录。

## 后端配置
1. **导入项目**：使用IDEA打开解压后的项目，配置Maven路径，等待JAR包依赖下载完成。
2. **配置Nacos**：
   - 下载Nacos 2.0.3版本，解压并配置MySQL数据库。
   - 修改Nacos配置文件，设置数据库连接信息。
   - 启动Nacos服务。

## 启动项目
1. **启动网关**：
   - 修改Nacos中的ruoyi-gateway-dev.yml，配置Redis连接信息。
   - 启动RuoYiGatewayApplication。
2. **启动登录模块**：
   - 修改ruoyi-auth-dev.yml，配置Redis连接信息。
   - 启动RuoYiAuthApplication。
3. **启动系统模块**：
   - 导入数据库表，配置MySQL连接信息。
   - 启动RuoYiSystemApplication。

## 前端配置
1. **打开VSCode**：确保本地已安装Node环境。
2. **导入项目**：导入ruoyi-ui项目。
3. **启动前端**：
   - 在终端输入`npm install`安装依赖。
   - 输入`npm run dev`启动前端服务。

## 访问系统
在浏览器中输入`localhost:80`，即可访问部署成功的若依微服务系统。

## 注意事项
- 确保所有配置文件中的数据库和Redis连接信息正确。
- 如果Nacos不在本地部署，需修改bootstrap.yml中的Nacos配置。

通过以上步骤，您可以顺利部署并运行若依开源框架的微服务版本。

## 下载链接

[若依开源框架-微服务版本ruoyi-Cloud使用说明-超详细](https://pan.quark.cn/s/2319f5819cf4)