---
layout: post
title: "详解Nexus的安装创建与配置宿主仓库及Maven项目"
date:   2020-01-29
tags: [Nexus,仓库,Maven,创建,安装]
comments: true
author: admin
---
# 详解Nexus的安装、创建与配置宿主仓库及Maven项目

本文详细介绍了如何安装Nexus Repository Manager，并指导读者如何创建和配置宿主仓库，以及如何使用Nexus来创建和管理Maven项目。通过本文，您将了解Nexus的基本功能和操作步骤，帮助您更好地管理和控制软件组件和依赖项。

## 一、Nexus的介绍

Nexus Repository Manager（简称Nexus）是Sonatype公司开发的一款强大仓库管理器，它简化了仓库维护，强化了私有仓库管理。通过Nexus，用户可集中管理、控制并访问软件组件和依赖项，确保私有仓库的安全稳定。Nexus提供权限控制和访问限制，防止未经授权的访问，增强数据保护。它还支持缓存和代理设置，提升内部网络下载速度，与构建工具和IDE无缝集成，方便开发人员获取依赖项。

## 二、Nexus的安装步骤

1. **下载Nexus**：
   - 从Nexus官网下载链接或使用百度网盘链接下载Nexus安装包。
   - 解压下载的文件，并将其放置在合适的位置。

2. **安装并启动Nexus**：
   - 打开命令提示符，切换到Nexus的bin目录。
   - 执行命令 `nexus.exe /install` 安装Nexus服务。
   - 执行命令 `nexus.exe /start` 启动Nexus服务。

3. **访问Nexus**：
   - 打开浏览器，输入 `http://localhost:8081/` 访问Nexus管理界面。
   - 使用默认用户名 `admin` 和默认密码登录。

## 三、配置宿主仓库

1. **创建宿主仓库**：
   - 在Nexus管理界面中，选择“Repositories”选项。
   - 点击“Create repository”按钮，选择“maven2 (hosted)”类型。
   - 填写仓库的ID、Name以及仓库策略（release或snapshot）。
   - 点击“Save”按钮完成创建。

2. **添加权限**：
   - 在“Security”选项中，点击“Privileges”。
   - 点击“Add”按钮，选择“Repository Target Privileges”添加发布版和快照版权限。

3. **创建角色和用户**：
   - 创建具有相应权限的角色。
   - 创建用户，并设置用户ID和密码。

## 四、修改setting.xml文件

1. **配置远程仓库认证**：
   - 打开Maven的 `settings.xml` 文件。
   - 在 `servers` 标签下添加远程仓库的用户名和密码配置。

## 五、创建Maven项目

1. **创建项目**：
   - 使用Maven命令创建一个新的Maven项目。
   - 配置项目的 `pom.xml` 文件，指定远程仓库的ID。

2. **编译与测试**：
   - 使用Maven命令编译源代码并运行测试案例。

3. **代码打包**：
   - 使用Maven命令将代码打包成jar文件，并安装到本地仓库。

通过以上步骤，您可以成功安装并配置Nexus，创建和管理Maven项目，实现高效的依赖管理和项目构建。