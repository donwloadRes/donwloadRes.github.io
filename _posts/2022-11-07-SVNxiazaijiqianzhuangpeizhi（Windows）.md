---
layout: post
title: "SVN下载及其安装配置（Windows）"
date:   2023-07-02
tags: [安装,SVN,客户端,下载,语言包]
comments: true
author: admin
---
# SVN下载及其安装配置（Windows）

本文档提供了SVN（Subversion）在Windows系统上的下载、安装及配置指南，并包括了SVN中文语言包的安装步骤。SVN是一个开源的版本控制系统，广泛用于软件开发项目中，帮助团队管理和跟踪代码的变化。

## 目录
1. [安装SVN前需知](#安装svn前需知)
2. [下载SVN服务器](#下载svn服务器)
3. [下载SVN客户端](#下载svn客户端)
4. [下载中文语言包](#下载中文语言包)
5. [服务器端的安装（Windows）](#服务器端的安装windows)
6. [客户端的安装（Windows）](#客户端的安装windows)
7. [中文语言包的安装](#中文语言包的安装)

## 安装SVN前需知
SVN的安装分为客户端和服务端两部分。一般情况下，只需要安装客户端即可。常用的客户端又分为两种：一种是安装在操作系统中的客户端，另一种是Eclipse插件或IDEA的插件。

## 下载SVN服务器
1. 进入官网：[VisualSVN Server](https://www.visualsvn.com/server/)
2. 点击“version history”历史版本，一般使用软件使用的是最新版本的上一个版本。
3. 选择4.2.0版本，选择64位点击下载。
4. 进入下载，等待下载完成即可。

## 下载SVN客户端
TortoiseSVN是Apache Subversion（SVN）客户端，实现为Windows Shell扩展。它直观且易于使用，因为它不需要运行Subversion命令行客户端。
1. 进入官网：[TortoiseSVN](https://tortoisesvn.net/)
2. 点击“downloads”进入下载页面。
3. 往下拉找到“older releases”老版本。
4. 选择想要的版本（推荐下载最新版本的上一个版本）。
5. 点击“Application”进入。
6. 根据电脑系统位数选择对应的下载即可。

## 下载中文语言包
1. 在客户端下载页面中选择“Language Packs”语言包。
2. 选择简体中文。

## 服务器端的安装（Windows）
1. 选择对应的版本，双击运行。
2. 点击“next”，勾选协议点击“next”。
3. 选择SVN服务器和管理控制台或只有管理控制权限，然后点击“next”。
4. 选择自己要安装路径、库路径、端口号、备份、协议（可以直接全部默认）。
5. 选择默认的使用用户和密码进行认证。
6. 进行安装，安装成功。
7. 服务器管理界面：Reposotories（资源库）、User（用户）、Groups（组）。
8. 右击此电脑-->管理，在服务里面可以看到SVN的服务（安装成功）。

## 客户端的安装（Windows）
1. 选择安装版本。
2. 点击“next”下一步。
3. 选择安装路径。
4. 进行安装，提示杀毒：允许即可。

## 中文语言包的安装
1. 安装VC++2015需要升级安装，安装这个即可，傻瓜式下一步就可以。
2. 安装语言包。
3. 切换中英文（桌面右击选择）。

通过以上步骤，您可以在Windows系统上成功安装并配置SVN，并使用中文语言包进行操作。

## 下载链接

[SVN下载及其安装配置Windows分享](https://pan.quark.cn/s/7c50de51a196)