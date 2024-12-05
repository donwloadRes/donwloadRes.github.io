---
layout: post
title: "DVWA下载及安装教程  图文详解配合phpStudy配置"
date:   2021-06-04
tags: [DVWA,phpStudy,Web,---,php]
comments: true
author: admin
---
# DVWA下载及安装教程 —— 图文详解配合phpStudy配置

---

## 概览

Damn Vulnerable Web Application (DVWA) 是一款专为安全研究者和Web开发者设计的不安全Web应用平台。它包含了多种常见的Web安全漏洞，如SQL注入、跨站脚本(XSS)、文件包含等，供学习和测试安全防御机制使用。本教程将引导您如何下载、安装DVWA，并配置phpStudy环境，以便您可以安全地进行渗透测试和提高您的Web安全知识。

---

### 准备工作

- **phpStudy**: 一个集成的PHP环境，包含Apache、MySQL等，简化了本地Web服务的搭建。
- **DVWA下载**: 从官方渠道或提供的链接下载最新版本的DVWA压缩包。

---

### 步骤分解

#### 1. 安装phpStudy
- 访问phpStudy官方网站下载适合您操作系统的版本并安装。
- 启动phpStudy，确保Apache和MySQL服务正在运行。

#### 2. 下载DVWA
- 推荐通过官方或稳定第三方源下载DVWA的ZIP文件。
- 下载完成后，解压至phpStudy的 WWW 目录下，通常位于 `phpstudy_pro/WWW` 或 `PHPTutorial/WWW`，具体取决于您使用的phpStudy版本。

#### 3. 配置DVWA
- 进入解压后的DVWA目录下的 `config` 文件夹。
- 复制 `config.inc.php.dist` 并重命名为 `config.inc.php`。
- 编辑 `config.inc.php` 文件，设置数据库用户名（默认root）和密码（如果是默认安装则为空），以及数据库名称（如dvwa）。

#### 4. 创建数据库
- 使用phpMyAdmin或者命令行进入MySQL，创建名为dvwa的数据库。
- 若DVWA提供了数据库脚本，需导入此脚本来初始化表结构。

#### 5. 初始化DVWA
- 打开浏览器，访问 `http://localhost/DVWA/setup.php`。
- 按照屏幕指示完成数据库的创建或重置。
  
#### 6. 访问DVWA
- 数据库配置无误后，通过访问 `http://localhost/DVWA/login.php` 进行登录，默认凭证为 `admin/password`。
- 第一次登录后建议调整安全级别（Low, Medium, High, Impossible），以适合您的学习或测试需求。

---

### 注意事项

- 在非专用测试环境中运行DVWA可能会造成安全风险，请确保不在生产环境中部署。
- 学习期间，了解每种漏洞的原理及其预防措施至关重要。
- 不断实践是掌握Web安全的关键，但务必遵守法律法规，不得在未经授权的系统上进行渗透测试。

---

通过以上步骤，您现在应该能够顺利地在本地搭建好DVWA环境，为您的网络安全学习之旅奠定坚实的基础。记得持续探索和实践，安全路上，永不停歇。

## 下载链接

[DVWA下载及安装教程图文详解配合phpStudy配置](https://pan.quark.cn/s/a0a4c0f8f316)