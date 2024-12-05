---
layout: post
title: "自定义数据类型的OpenDDS实例Win10"
date:   2024-06-07
tags: [OpenDDS,配置文件,自定义,实例,数据类型]
comments: true
author: admin
---
# 自定义数据类型的OpenDDS实例（Win10）

本仓库提供了一个自定义数据类型的OpenDDS实例，适用于Windows 10操作系统。该实例包含了基于对等发现和集中发现的配置文件，方便用户快速上手和测试。

## 资源文件描述

- **标题**: 自定义的数据类型的OpenDDS实例_WIN10
- **描述**: 该资源文件包含了自定义数据类型的OpenDDS实例，运行环境为Win10。实例中包含了两种发现机制的配置文件：对等发现和集中发现。编译完成后，用户只需执行`./Publisher`和`./Subscriber`即可启动对等发现模式，默认情况下会自动加载`config_Pub.ini`和`config_Sub.ini`配置文件。

## 使用说明

1. **编译**: 按照OpenDDS的编译流程进行编译，确保所有依赖项已正确安装。
2. **运行**: 编译完成后，在命令行中执行以下命令：
   - 启动发布者: `./Publisher`
   - 启动订阅者: `./Subscriber`
3. **配置文件**: 默认情况下，`./Publisher`和`./Subscriber`会自动加载`config_Pub.ini`和`config_Sub.ini`配置文件。用户可以根据需要修改这些配置文件以适应不同的网络环境。

## 注意事项

- 确保运行环境为Windows 10，且已正确安装OpenDDS及相关依赖。
- 配置文件的路径和内容可以根据实际需求进行调整。

## 参考资料

有关OpenDDS的更多信息和配置说明，请参考相关文档和教程。

## 下载链接

[自定义数据类型的OpenDDS实例Win10](https://pan.quark.cn/s/6ef33f4ca078)