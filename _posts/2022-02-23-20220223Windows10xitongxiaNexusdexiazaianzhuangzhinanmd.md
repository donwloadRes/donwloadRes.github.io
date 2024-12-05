---
layout: post
title: "Windows 10系统下Nexus的下载安装指南"
date:   2021-12-10
tags: [Nexus,Windows,10,Maven,nexus]
comments: true
author: admin
---
# Windows 10系统下Nexus的下载安装指南

本文档详细介绍了如何在Windows 10系统下下载和安装Nexus。Nexus是一个常用的仓库管理工具，广泛应用于Maven私服的搭建和管理。以下是详细的安装步骤和注意事项。

## 1. 下载Nexus

Nexus可以从官方网站或百度网盘下载。官方网站下载速度较慢，建议使用百度网盘链接进行下载。下载完成后，文件将以压缩包的形式提供。

## 2. 解压安装

下载完成后，直接解压压缩包。解压后会生成两个目录：
- `nexus-3.18.1-01`：包含Nexus运行所需的文件，如启动脚本和依赖项。
- `sonatype-work`：运行时目录，用于生成运行时所需的数据。

## 3. 启动Nexus

打开命令提示符（cmd），切换到解压后的目录中的`bin`文件夹，运行以下命令启动Nexus：
```
nexus.exe /run
```
启动成功后，会显示“Started Sonatype Nexus OSS 3.18.1-01”的提示信息。

## 4. 配置环境变量（可选）

为了方便以后的使用，可以将Nexus的安装路径配置到系统的环境变量`PATH`中。

## 5. 登录Nexus

启动成功后，打开浏览器访问`http://localhost:8081`即可进入Nexus的管理界面。初始管理员账号为`admin`，密码默认位于以下文件中：
```
nexus-3.18.1-01-win64\sonatype-work\nexus3\admin.password
```
首次登录后，系统会提示修改密码。

## 6. 创建仓库

登录后，可以根据需要创建和管理仓库。Nexus支持多种类型的仓库，如Maven、npm等。

## 注意事项

- 确保系统已安装JDK 8或更高版本。
- 首次登录后务必修改默认密码。
- 可以根据需要将Nexus配置为Windows服务，以便开机自动启动。

通过以上步骤，您可以在Windows 10系统下成功安装和配置Nexus，开始使用它来管理您的Maven私服。

## 下载链接

[Windows10系统下Nexus的下载安装指南](https://pan.quark.cn/s/3ac998eabef3)