---
layout: post
title: "SecureCRT安装与使用教程"
date:   2020-10-15
tags: [SecureCRT,登录,教程,点击,日志]
comments: true
author: admin
---
# SecureCRT安装与使用教程

本仓库提供了一个资源文件，包含SecureCRT的安装与使用教程。SecureCRT是一款支持SSH（SSH1和SSH2）的终端仿真程序，广泛应用于Windows下登录UNIX或Linux服务器主机的场景。

## 资源内容

- **SecureCRT安装包**：无需安装，直接解压即可使用。
- **使用教程**：详细介绍了如何远程登录另一台Linux电脑，以及如何监听串口信息。

## 使用步骤

### 一、获取SecureCRT汉化版

1. 将文件放在D盘。
2. 双击`SecureCRTPortable.exe`，即可使用。

### 二、远程登录另一台Linux电脑

1. 打开SecureCRT软件，点击“快速连接”。
2. 填写要远程登录的另一台电脑的IP地址和用户名，点击连接按钮。
3. 输入远程登录电脑的开机密码，勾选保存密码，点击确定按钮。
4. 远程登录成功后，显示如下图所示。

### 三、监听串口信息

1. 串口连接电脑，打开设备管理器，查看端口号。
2. 打开SecureCRT软件，选择“快速连接”，协议选择Serial，选择设备管理器出现的端口号，选择对应的波特率，点击连接按钮。
3. 保存日志：点击菜单栏里的选项，选择会话选项—日志文件，设置日志文件路径和格式，即可在每一次开始连接的时候记录并保存日志。

## 注意事项

- 本资源为绿色便携版，无需安装，解压后即可使用。
- 使用过程中请确保网络连接正常，且目标服务器或设备处于可访问状态。

## 贡献

欢迎提交问题和建议，帮助改进本资源文件。

---

通过本教程，您可以轻松掌握SecureCRT的安装与使用，实现远程登录和管理Linux服务器。

## 下载链接

[SecureCRT安装与使用教程](https://pan.quark.cn/s/56ba63afcdfb)