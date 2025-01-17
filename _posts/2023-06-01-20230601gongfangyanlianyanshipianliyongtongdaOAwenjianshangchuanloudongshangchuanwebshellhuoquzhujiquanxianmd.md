---
layout: post
title: "攻防演练演示篇利用通达OA文件上传漏洞上传webshell获取主机权限"
date:   2022-10-23
tags: [OA,上传,通达,漏洞,webshell]
comments: true
author: admin
---
# 攻防演练演示篇：利用通达OA文件上传漏洞上传webshell获取主机权限

## 简介
本资源文件旨在演示如何利用通达OA（Office Anywhere）系统中的文件上传漏洞，上传webshell以获取主机权限。通过此演示，用户可以了解该漏洞的利用过程，并学习如何防范此类攻击。

## 环境要求
1. 靶机环境：Windows 10
2. 通达OA版本：11.6
3. 攻击机需要安装Java环境

## 演示步骤

### 1. 靶机部署通达OA 11.6
- 下载并安装通达OA 11.6。
- 安装完成后，访问`http://127.0.0.1`验证安装成功。

### 2. 攻击机部署蚁剑
- 下载并安装蚁剑工具。

### 3. 攻击机部署Java环境
- 下载并安装Java环境。

### 4. 红方操作
#### 4.1 上传webshell
- 使用通达OA综合利用工具TDOA_RCE.exe，填入靶机URL地址，点击获取cookie。
- 自动填充cookie值后，选择后台上传getshell，点击一键利用，上传webshell。

#### 4.2 连接webshell
- 打开蚁剑，右键添加数据，填入webshell地址和连接密码，测试连接，发现连接成功。
- 添加数据成功后，可以进行任意操作，如访问文件系统。

### 5. 蓝方操作
#### 5.1 检查后门情况
- 运维安全人员使用火绒对网站根目录进行扫描，检查是否存在后门程序。
- 发现后门文件后，进行删除。

#### 5.2 根治漏洞
- 对通达OA漏洞情况进行自检，发现高危漏洞后进行升级，从而根治该漏洞。

## 注意事项
- 本演示仅供学习和研究使用，请勿用于非法用途。
- 使用本资源文件造成的任何后果，由使用者自行承担。

## 相关资源
- 本文用到的环境+工具可在百度网盘下载链接中获取。

---

通过本资源文件，用户可以深入了解通达OA文件上传漏洞的利用过程，并学习如何防范此类攻击。希望本资源对您的学习和研究有所帮助。

## 下载链接

[攻防演练演示篇利用通达OA文件上传漏洞上传webshell获取主机权限](https://pan.quark.cn/s/240101a3ed6e)