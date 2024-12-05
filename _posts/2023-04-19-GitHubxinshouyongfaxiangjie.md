---
layout: post
title: "GitHub新手用法详解"
date:   2023-09-15
tags: [git,GitHub,Git,Bash,master]
comments: true
author: admin
---
# GitHub新手用法详解

本文详细介绍了GitHub的基本用法，适合新手入门。通过阅读本文，您将了解如何注册GitHub账号、创建仓库、上传文件、管理分支、发起Pull Request、处理Issue以及使用Wiki等功能。

## 目录

1. **GitHub登录与注册**
   - GitHub属于国外平台，注册时需使用邮箱，建议使用QQ邮箱。
   - 官网为英文界面，建议使用谷歌浏览器翻译网页。

2. **创建仓库**
   - 登录后可创建自己的仓库，分为公有和私有两种，根据需求选择。

3. **Git Bash安装步骤详解**
   - Git Bash是Windows下的命令行工具，用于Git版本控制。
   - 下载并安装Git Bash，安装完成后右键文件夹可使用Git Bash。

4. **Git Bash常用命令**
   - `git init`：初始化Git仓库。
   - `git clone`：获取远程项目并下载到本地。
   - `git status`：查看本地修改与服务器的差异。
   - `git add`：将差异文件添加以便提交。
   - `git commit -m "注释"`：提交更改到服务器。
   - `git checkout master`：切换到master分支。
   - `git pull`：获取服务器最新更改到本地。
   - `git merge local master`：将本地local分支合并到远程master分支。
   - `git push origin master`：正式提交到远程master服务器。

5. **获取SSH密钥**
   - 使用命令`ssh-keygen -t rsa -C "git账号"`生成SSH密钥。
   - 将生成的SSH密钥绑定到GitHub账号。

6. **代码克隆与提交**
   - 使用`git clone`命令将仓库克隆到本地。
   - 在本地创建文件并使用Git Bash提交到GitHub仓库。

通过以上步骤，您可以轻松掌握GitHub的基本用法，开始您的代码托管和协作之旅。

## 下载链接

[GitHub新手用法详解](https://pan.quark.cn/s/7d8c3ee7d33b)