---
layout: post
title: "Windows 安装 Tomcat 85 指南"
date:   2022-07-03
tags: [Tomcat,8.5,安装,安装包,Windows]
comments: true
author: admin
---
# Windows 安装 Tomcat 8.5 指南

本资源文件提供了在Windows系统上安装Tomcat 8.5的详细步骤和相关配置说明。Tomcat是一个开源的Web应用服务器，广泛用于开发和部署Java Web应用程序。

## 安装前准备

1. **安装包下载**
   - 从官网下载Tomcat 8.5的安装包。
   - 或者使用提供的百度网盘下载链接（提取码: h9jr）。

2. **OpenJDK安装**
   - 确保系统中已安装OpenJDK，Tomcat需要Java环境支持。

## 安装步骤

1. **双击安装包**
   - 运行下载的安装包，按照提示完成安装。
   - 安装完成后，点击“Finish”。

2. **查看服务并修改启动类型**
   - 使用快捷键 `Win + R` 打开运行窗口，输入 `services.msc`。
   - 在服务窗口中找到Tomcat服务。
   - 右键点击Tomcat服务，选择“属性”，将启动类型设置为“自动”。

3. **测试安装**
   - 打开浏览器，输入 `http://localhost:8080/`。
   - 登录后台，输入安装时配置的用户名和密码。

## 修改端口号和密码

1. **修改端口号**
   - 打开 `D:\Tomcat 8.5\conf\server.xml` 文件，修改端口号。

2. **修改密码**
   - 打开 `D:\Tomcat 8.5\conf\tomcat-users.xml` 文件，修改管理员密码。

## 卸载Tomcat

1. **卸载Tomcat服务**
   - 进入 `D:\Tomcat 8.5\bin\` 目录。
   - 运行 `service.bat remove Tomcat8` 命令卸载服务。

2. **卸载Tomcat程序（不推荐）**
   - 进入 `D:\Tomcat 8.5\` 目录。
   - 运行 `Uninstall.exe -ServiceName="<Tomcat8>"` 命令卸载程序。

通过以上步骤，您可以在Windows系统上成功安装并配置Tomcat 8.5，开始您的Java Web应用开发之旅。

## 下载链接

[Windows安装Tomcat8.5指南分享](https://pan.quark.cn/s/638ca294bc2d)