---
layout: post
title: "SQLi-Labs 靶场搭建教程"
date:   2022-11-19
tags: [靶场,sqli,labs,SQLi,Labs]
comments: true
author: admin
---
# SQLi-Labs 靶场搭建教程

本教程详细介绍了如何搭建 SQLi-Labs 靶场，帮助用户学习和练习 SQL 注入漏洞。SQLi-Labs 是一个开源应用程序，提供了一系列的漏洞场景和练习环境，帮助用户了解和实践 SQL 注入漏洞的利用技术。

## 环境准备

建议采用虚拟机作为靶场环境的承载平台，以实现更灵活、可定制的配置，提高系统资源的利用效率。通过虚拟化技术，靶场环境的部署与管理变得更为高效，同时减少了对物理资源的占用，为安全研究和实践提供了更为便捷的条件。

## 安装步骤

1. **安装 PHPStudy**  
   可以参考以下文章来安装 PHPStudy：
   - 如何搭建 Pikachu 靶场保姆级教程（附链接）

2. **安装 sqli-labs**  
   点击链接下载 sqli-labs，将其解压缩到 WWW 目录下并改名为 sqli-labs。进入文件内找到 `db-creds.inc` 文件，打开文件并修改数据库配置信息。

3. **访问 sqli-labs 靶场**  
   打开 PHPStudy，点击网址，点击创建网站。域名输入 sqli-labs，端口号改为别的避免冲突。选择 PHP 版本并安装，最后点击确定即可。

4. **初始化 sqli-labs 靶场**  
   点击图中选项，出现初始化成功的画面。

## 注意事项

- 确保 PHP 版本与 sqli-labs 兼容。
- 数据库配置信息需与实际环境一致。

通过本教程，用户可以快速搭建 SQLi-Labs 靶场，进行 SQL 注入漏洞的学习和实践。

## 下载链接

[SQLi-Labs靶场搭建教程](https://pan.quark.cn/s/1afc38b3e09d)