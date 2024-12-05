---
layout: post
title: "基于安卓AndroidStudio在线订餐app设计"
date:   2020-05-18
tags: [管理员,用户,菜品,安卓,模拟器]
comments: true
author: admin
---
# 基于安卓AndroidStudio在线订餐app设计

## 项目描述

本项目是一个基于安卓平台的在线订餐应用设计，使用Idea2021、AndroidStudio2021、Mysql5.6和夜神模拟器进行开发。项目包含两个主要身份：管理员和用户。

### 管理员功能

管理员通过Web端操作系统，主要功能包括：

- **角色维护**：超级管理员可以添加其他角色，如菜谱管理员等。
- **系统菜单维护**：管理员可以维护系统菜单。
- **角色权限分配**：管理员可以分配不同角色的权限。
- **菜品信息管理**：管理员可以上传并添加新的菜品。
- **订单管理**：管理员可以查询用户的下单记录。

### 用户功能

用户通过安卓手机端操作，主要功能包括：

- **注册账号**：用户可以注册新账号。
- **登录系统**：用户登录后可以进行操作。
- **分类查询菜谱**：用户可以按分类查询菜谱列表。
- **购物车功能**：用户可以选择自己喜欢的菜品加入购物车。
- **提交订单**：用户可以提交结算订单。
- **个人中心**：用户可以查询自己的订单记录。

## 使用说明

### Web端登录

- **登录地址**：http://localhost:8088/toLogin
- **超级管理员账号密码**：admin/123
- **菜品管理员账号密码**：t1/123

### 手机端用户

- **用户账号密码**：user1/123

## 注意事项

- 请确保所有开发环境已正确配置。
- 在运行项目前，请确保数据库已正确连接。
- 使用夜神模拟器进行安卓端测试时，请确保模拟器已正确启动并与开发环境连接。

## 项目结构

- **Web端**：主要负责管理员操作，包括角色管理、菜单管理、权限分配、菜品管理和订单管理。
- **安卓端**：主要负责用户操作，包括注册、登录、菜谱查询、购物车、订单提交和个人中心。

## 开发环境

- Idea2021
- AndroidStudio2021
- Mysql5.6
- 夜神模拟器

## 贡献

欢迎任何形式的贡献，包括但不限于代码优化、功能扩展、文档完善等。请通过提交Issue或Pull Request来参与项目。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[基于安卓AndroidStudio在线订餐app设计](https://pan.quark.cn/s/fecb1e2c23ae)