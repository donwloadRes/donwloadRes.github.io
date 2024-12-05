---
layout: post
title: "Navicat Mac版密码保存失败解决方案"
date:   2021-06-24
tags: [Navicat,密码,Mac,保存,Premium]
comments: true
author: admin
---
# Navicat Mac版密码保存失败解决方案

## 简介

在使用Navicat for Mac时，可能会遇到无法保存密码的问题，提示“failed to save password error code -34018”。本文将详细介绍如何解决这一问题，并提供相关资源文件的下载。

## 问题描述

Navicat for Mac在某些版本中，可能会出现无法保存数据库连接密码的情况，具体表现为在保存密码时弹出错误提示“failed to save password error code -34018”。这会导致每次连接数据库时都需要手动输入密码，给用户带来不便。

## 解决方案

### 1. 清除残留的Navicat钥匙串

如果之前连接过数据库，可能会在钥匙串中留下残留的钥匙串信息。需要手动删除这些残留信息。

1. 打开“钥匙串访问”应用程序。
2. 在右上角的搜索框中输入“Navicat”。
3. 如果有相关结果，删除这些钥匙串信息。

### 2. 安装旧版本Navicat并保存密码

1. 下载并安装Navicat Premium 15.0.20.1版本。
2. 连接数据库并保存密码。
3. 退出Navicat。

### 3. 安装新版本Navicat

1. 下载并安装最新版本的Navicat Premium for Mac。
2. 运行Navicat，此时会提示“Navicat Premium 想要使用您存储在钥匙串的 xxxx 机密信息”。
3. 输入Mac的开机密码，并点击“始终允许”。

### 4. 完成

通过以上步骤，即可解决Navicat for Mac无法保存密码的问题。

## 资源文件

本仓库提供了解决方案中所需的旧版本Navicat Premium 15.0.20.1版本的下载资源。请根据需要下载并安装。

## 注意事项

- 确保在安装新版本Navicat之前，已经使用旧版本保存了数据库连接密码。
- 如果之前安装过Navicat，建议使用卸载和清理软件进行彻底卸载。

## 参考资料

本文参考了CSDN博客文章《Navicat mac版无法保存密码 提示“failed to save password error code -34018”的解决办法》，详细步骤请参考原文。

---

希望本文能帮助您顺利解决Navicat for Mac密码保存失败的问题。

## 下载链接

[NavicatMac版密码保存失败解决方案分享](https://pan.quark.cn/s/c55b144ea83e)