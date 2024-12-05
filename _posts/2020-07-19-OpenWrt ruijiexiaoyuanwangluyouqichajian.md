---
layout: post
title: "OpenWrt 锐捷校园网路由器插件"
date:   2022-08-30
tags: [插件,mentohust,OpenWrt,路由器,校园网]
comments: true
author: admin
---
# OpenWrt 锐捷校园网路由器插件

## 资源描述

本仓库提供了一个适用于A53平台的OpenWrt路由器插件，用于锐捷校园网的认证。资源文件解压后包含两个主要组件：`mentohust`插件和`luci-app-mentohust`控制插件。

## 使用说明

1. **安装mentohust插件**：
   - 首先，将解压后的`mentohust`插件上传到你的OpenWrt路由器。
   - 在OpenWrt的Web界面中，进入“系统” -> “软件包”，点击“上传软件包”，选择并上传`mentohust`插件文件。
   - 上传完成后，点击“安装”按钮进行安装。

2. **安装luci-app-mentohust控制插件**：
   - 同样地，将解压后的`luci-app-mentohust`控制插件上传到你的OpenWrt路由器。
   - 在OpenWrt的Web界面中，进入“系统” -> “软件包”，点击“上传软件包”，选择并上传`luci-app-mentohust`插件文件。
   - 上传完成后，点击“安装”按钮进行安装。

3. **配置mentohust认证**：
   - 安装完成后，在OpenWrt的Web界面中，进入“服务”菜单，你应该能够看到“MentoHUST”选项。
   - 点击“MentoHUST”进入配置页面，输入你的校园网账号和密码，并根据需要配置其他选项。
   - 保存配置后，启动MentoHUST服务，即可完成校园网的认证。

## 注意事项

- 请确保你的路由器CPU架构为A53，否则可能无法正常使用该插件。
- 在安装插件之前，建议备份你的OpenWrt配置，以防出现意外情况。
- 如果在使用过程中遇到问题，可以尝试重启路由器或重新安装插件。

## 更新日志

- **版本1.0**（初始版本）：
  - 提供mentohust插件和luci-app-mentohust控制插件。
  - 支持A53平台OpenWrt路由器的锐捷校园网认证。

## 联系我们

如果在使用过程中遇到任何问题，欢迎通过GitHub的Issues功能提交反馈。我们将尽快回复并提供帮助。

## 下载链接

[OpenWrt锐捷校园网路由器插件](https://pan.quark.cn/s/133fc346036a)