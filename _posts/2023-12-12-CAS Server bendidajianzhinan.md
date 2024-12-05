---
layout: post
title: "CAS Server 本地搭建指南"
date:   2023-06-13
tags: [CAS,Server,解压,文件,zip]
comments: true
author: admin
---
# CAS Server 本地搭建指南

本资源文件提供了一个详细的指南，帮助您在本地环境中搭建CAS Server。CAS（Central Authentication Service）是一个开源的单点登录（SSO）解决方案，广泛应用于企业级应用中。

## 内容概述

1. **下载与解压**：
   - 提供了CAS Server的zip文件下载链接。
   - 使用BandZip等压缩软件解压文件。

2. **配置域名映射**：
   - 在Windows系统中配置hosts文件，实现本地域名映射。

3. **运行CAS Server**：
   - 通过命令行运行CAS Server，确保JDK和Maven环境变量已配置。

4. **访问与登录**：
   - 使用浏览器访问CAS Server的登录页面。
   - 提供了默认的用户名和密码。

## 使用步骤

1. **下载zip文件**：
   - 从提供的链接下载CAS Server的zip文件。

2. **解压到磁盘**：
   - 使用压缩软件将下载的zip文件解压到本地磁盘。

3. **配置域名映射**：
   - 打开hosts文件（路径：C:\Windows\System32\drivers\etc\hosts），添加域名映射。

4. **运行CAS Server**：
   - 进入解压后的主目录，通过命令行输入`build.cmd run`运行CAS Server。

5. **访问CAS Server**：
   - 在浏览器中输入`http://cas.server.com:8443/cas/login`访问登录页面。
   - 使用默认用户名`casuser`和密码`Mellon`进行登录。

## 注意事项

- 确保JDK和Maven的环境变量已正确配置。
- 可以根据需要修改配置文件，实现更复杂的认证方式。

通过本指南，您可以轻松地在本地环境中搭建并运行CAS Server，为后续的开发和测试提供基础支持。

## 下载链接

[CASServer本地搭建指南](https://pan.quark.cn/s/6e2ae9d9a457)