---
layout: post
title: "Idea热加载插件JRebel激活及使用教程"
date:   2022-08-21
tags: [JRebel,插件,激活,IDEA,服务器]
comments: true
author: admin
---
# Idea热加载插件JRebel激活及使用教程

## 概述

本文档提供了详尽的指导，旨在帮助开发者学会如何下载、激活并有效使用JRebel插件于IntelliJ IDEA中，以实现Java项目的热部署功能。JRebel是一款强大的插件，能够显著提升开发效率，允许开发者在不重启应用的前提下查看代码变更的效果，尤其适合长时间的迭代开发和大型项目维护。

## 安装JRebel插件

1. **插件市场查找**: 打开IntelliJ IDEA的设置/Preferences，导航至Plugins部分。
2. **搜索JRebel**: 在Marketplace中键入“JRebel”，找到官方插件并安装。
3. **重启IDE**: 安装完成后，需重启IDE以使插件生效。

## 激活JRebel

1. **获取激活方式**: 插件激活通常需要有效的许可证。文中提及的方法涉及搭建本地激活服务器或利用特定的jar包生成授权地址。
2. **配置License Server**: 使用提供的激活jar包，在本地或服务器上运行，并通过开放相应端口(如1008)来获得激活地址。
3. **填写邮箱激活**: 根据指引，输入任意邮箱地址，连同生成的特定token，完成激活流程。

## 设置自动编译与JRebel配置

- **自动编译**: 在`Settings/Preferences > Build, Execution, Deployment > Compiler`中启用“Build project automatically”。
- **允许自动make**: 确保`Settings/Preferences > Advanced Settings > Compiler`中的“Allow auto-make to start even if developed application is currently running”被勾选。

## 使用JRebel进行热部署

- **本地热部署**: 成功激活并配置后，JRebel图标出现在IDE侧边栏，勾选项目进行本地热部署设置。运行项目时，会在指定目录生成`.rebel.xml`配置文件。
- **远程热部署**: 需要在远程服务器上同样安装JRebel，并正确配置远程连接的密码及相应的Javaagent路径。通过IDEA配置远程服务器详情，实现代码更改即时生效。

## 注意事项

- 确保IDEA工作在离线模式，以防激活失效。
- 对于多模块项目，确保所有依赖模块的变动都能正确反映，可能需要手动调整`rebel-remote.xml`配置文件。

通过以上步骤，您可以充分利用JRebel的功能，享受无缝的热部署体验，大幅减少开发循环时间，提高工作效率。记住，保持激活状态的有效性是持续享受这一便利的关键。

## 下载链接

[Idea热加载插件JRebel激活及使用教程分享](https://pan.quark.cn/s/f6822d7a02c1)