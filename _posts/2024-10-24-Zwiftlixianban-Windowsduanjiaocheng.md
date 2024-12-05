---
layout: post
title: "Zwift离线版-Windows端教程"
date:   2020-06-28
tags: [Zwift,离线,Windows,教程,Python]
comments: true
author: admin
---
# Zwift离线版-Windows端教程

## 概览
本资源提供了详细的指南，旨在帮助Windows用户在没有网络连接的情况下体验Zwift。Zwift是一款热门的室内骑行训练软件，通过本教程，您可以学会如何在离线模式下设置和运行Zwift，享受虚拟骑行的乐趣。

## 教程步骤概要

### 1. 安装Zwift
- 访问Zwift官方网站下载适合Windows的版本。
- 避免默认安装至C盘，推荐自定义安装路径，例如E:\Zwift。
- 安装完成后，启动Zwift，让它完成初始化并登录账户，随后退出。

### 2. 获取Zwift-offline
- 有两种获取方式：通过GitHub的Release页面下载Source code.zip，或使用提供的百度网盘链接。
- 解压缩文件至指定位置。

### 3. 设置Python环境
- 推荐安装Python 3.10版本，并确保Python添加至PATH环境变量。
- 创建或激活一个Python虚拟环境（可选）。
- 使用pip安装 zwift-offline 项目所需的依赖项，通过运行`pip install -r requirements.txt`。

### 4. 配置Hosts文件
- 以管理员身份运行`configure_client.bat`脚本来指向您的Zwift安装路径。
- 修改Hosts文件（位于C:\Windows\System32\drivers\etc\），以便使用离线服务器。

### 5. 运行Zwift-offline
- 导航至解压的zwift-offline文件夹，运行`standalone.py`文件以启动服务。
- 需要每次运行Zwift之前先执行此步骤。

### 6. 启动Zwift
- 在启动Zwift前，确保已运行离线服务器。
- 您将见到离线模式的界面，可选择地图和设置。

### 7. 个性化设置与Strava关联
- 在Zwift离线界面获取并导入您的个人信息和成就。
- 如需关联Strava账户，同样在设置内完成授权。

## 注意事项
- 请确保在进行每一步操作前仔细阅读相关指示，特别是关于环境配置和文件路径的设置。
- 确保Python环境设置正确，避免版本冲突。
- 对于遇到的问题，教程作者建议通过评论或私信交流解决。

通过本教程的指引，无论是新手还是高级用户，都可以顺利设置并享受Zwift的离线骑行体验。立即开始您的离线骑行之旅吧！

## 下载链接

[Zwift离线版-Windows端教程](https://pan.quark.cn/s/b4b93375836b)

## 下载链接

[Zwift离线版-Windows端教程](https://pan.quark.cn/s/0b3ba3d93d49)