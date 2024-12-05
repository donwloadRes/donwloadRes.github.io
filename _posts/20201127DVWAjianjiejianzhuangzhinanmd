---
layout: post
title: "DVWA简介及安装指南"
date:   2020-04-16
tags: [DVWA,Web,PHP,MySQL,安装]
comments: true
author: admin
---
# DVWA简介及安装指南

本资源提供了关于Damn Vulnerable Web Application（DVWA）的详尽介绍与安装步骤。DVWA是一个专为Web安全测试设计的PHP/MySQL应用，其核心目的在于为安全研究人员提供一个合法的环境，以测试他们的技能和工具，并教育Web开发者理解并加强网络安全措施。该应用内建了十种常见安全漏洞的示例，涵盖暴力破解、命令注入、CSRF、文件包含、文件上传、SQL注入等多个方面，完全覆盖OWASP TOP10漏洞，适合Web安全初学者至进阶人士使用。

## 安装环境需求

- **PHP环境**：推荐使用PHPStudy，一个集成PHP、Apache、MySQL等的一键式安装包，便于快速搭建PHP运行环境。
- **数据库**：MySQL，用于存储DVWA相关的数据。
- **源码**：从GitHub下载最新的DVWA源码压缩包。

## 安装步骤概述

### 1. PHPStudy安装
- 下载并安装PHPStudy，选择合适的位置安装，建议不在系统盘。
- 自动配置好PHP和MySQL环境，确保Apache和MySQL服务正常启动。

### 2. DVWA源码部署
- 解压缩DVWA的`.zip`文件，并将其重命名（可选）后移至PHPStudy的Web服务根目录（通常是`WWW`目录）。
- 在DVWA的`config`目录下，找到并更名`config.inc.php.dist`为`config.inc.php`。
- 编辑`config.inc.php`文件，根据个人MySQL设置修改数据库用户名和密码，默认推荐使用`root`。
  
### 3. 数据库配置
- 通过浏览器访问DVWA的安装地址，通常是你的IP地址加上/dvwa/setup.php路径，进行数据库的初始化。
- 创建或重置DVWA数据库，确保安装过程中所有表都被正确创建。

### 4. 访问与安全设置
- 成功安装后，可以通过访问你的IP地址加上/dvwa进入DVWA的登录界面，默认用户名为`admin`，密码为`password`。
- 进入后，你可以通过“DVWA Security”设置不同的安全性等级来挑战不同的安全场景。

## 注意事项
- 在进行实际的渗透测试前，请确保你拥有对测试环境的合法权限，避免非法入侵的风险。
- 根据你的具体环境，可能需要安装额外的VC运行库来支持特定版本的PHP。
- 若在安装过程中遇到问题，检查PHP和MySQL的版本兼容性，以及防火墙和端口配置。

通过以上步骤，你就能够成功搭建一个用于学习和实践Web安全测试的DVWA环境，助你在Web安全领域不断深入探索。

## 下载链接

[DVWA简介及安装指南](https://pan.quark.cn/s/f2f2368f81b3)