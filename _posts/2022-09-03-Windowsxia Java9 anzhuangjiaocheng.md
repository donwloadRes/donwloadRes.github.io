---
layout: post
title: "Windows下 Java9 安装教程"
date:   2020-12-15
tags: [安装,教程,Windows,JRE,bin]
comments: true
author: admin
---
# Windows下 Java9 安装教程

本仓库提供了一个详细的教程，帮助用户在Windows操作系统下安装Java 9。教程内容包括下载Java 9安装包、安装过程、配置环境变量以及测试安装是否成功。

## 教程内容

### 1. 下载Java 9安装包
- 下载地址：Oracle官方网站
- 备用下载：百度网盘链接（提取码：9hkz）

### 2. 安装Java 9
- 双击exe文件运行
- 更改安装路径（按自身需求更改）
- 注意：路径中不要有中文，尽量不要有空格
- 取消公共JRE的安装
- 开始安装

### 3. 配置环境变量
- 右键此电脑 -> 属性 -> 高级系统设置 -> 环境变量 -> 系统变量 -> 新建
- 变量名：JAVA_HOME
- 变量值：安装目录中bin目录的地址（不包含bin）
- 在path中添加 %JAVA_HOME%\bin

### 4. 测试安装
- 进入命令行，输入 `java -version`
- 输出以下内容，安装成功

## 注意事项
- 安装路径中不要有中文和空格，以免出现不必要的麻烦。
- 安装过程中取消公共JRE的安装，因为开发工具中已包含JRE。

## 贡献
欢迎提交问题和改进建议，帮助我们完善这个教程。

## 下载链接

[Windows下Java9安装教程](https://pan.quark.cn/s/5db20fc921fc)