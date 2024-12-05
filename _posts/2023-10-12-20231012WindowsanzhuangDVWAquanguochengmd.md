---
layout: post
title: "Windows安装DVWA全过程"
date:   2020-08-01
tags: [DVWA,安装,Windows,Web,PHPStudy]
comments: true
author: admin
---
# Windows安装DVWA（全过程）

本文详细介绍了如何在Windows系统上安装DVWA（Damn Vulnerable Web Application），这是一个用于安全测试和渗透测试的漏洞靶场。通过本文的步骤，您可以轻松地在本地环境中搭建一个DVWA环境，用于学习和实践Web安全技术。

## 安装步骤

### 1. 安装PHPStudy

1. 下载并安装PHPStudy软件。
2. 运行安装程序，设定安装路径（建议不要放在C盘）。
3. 安装完成后，启动Apache服务和MySQL服务进行测试。
4. 在浏览器中输入`127.0.0.1`或`localhost`，如果出现PHPStudy欢迎界面，则表示安装成功。

### 2. 下载并安装DVWA

1. 下载DVWA压缩包，解压后重命名为`dvwa`。
2. 将解压后的`dvwa`文件夹放入PHPStudy安装目录下的`www`文件夹中。
3. 修改DVWA配置文件`config.inc.php`，将数据库用户名和密码分别修改为`root`和`root`。

### 3. 配置DVWA

1. 在浏览器中输入`127.0.0.1/dvwa`，进入DVWA界面。
2. 点击`Setup/Reset DB`，然后点击`Create/Reset Database`，如果显示`Setup successful`，则表示配置成功。

### 4. 解决常见问题

1. **reCAPTCHA key: Missing**：在`config.inc.php`文件中找到相关代码，输入正确的reCAPTCHA key。
2. **PHP function allow_url_include: Disabled**：在PHP配置文件中将`allow_url_fopen`和`allow_url_include`设置为`On`，然后重启Apache服务。

### 5. 登录DVWA

1. 使用默认账号`admin`和密码`password`登录DVWA。
2. 登录成功后，您可以开始进行安全攻防演示和学习。

通过以上步骤，您已经成功在Windows系统上安装并配置了DVWA，可以开始进行Web安全测试和学习。

## 下载链接

[Windows安装DVWA全过程](https://pan.quark.cn/s/524975a54ace)