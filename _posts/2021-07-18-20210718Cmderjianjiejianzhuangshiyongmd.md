---
layout: post
title: "Cmder简介及安装使用"
date:   2022-10-22
tags: [Cmder,右键,zip,即可,使用]
comments: true
author: admin
---
# Cmder简介及安装使用

## 简介
Cmder是一款Windows下可代替cmd使用的命令行工具，支持Linux命令。它提供了更加美观和功能丰富的命令行界面，适合开发者和系统管理员使用。

## 安装包获取
1. **网盘已分享zip和7z格式**：
   - 链接：[此处省略链接]
   - 提取码：dmw1

2. **Full版本下载安装**：
   - 下载zip文件解压即可使用。
   - zip包解压缩后，双击Cmder.exe进行使用。

## 如何将Cmder添加到鼠标右键列表
1. **配置环境变量**：
   - 为了方便在任意目录下鼠标右键即可使用，需要添加环境变量。

2. **管理员身份运行cmd**：
   - 执行命令：`Cmder.exe /REGISTER ALL`

3. **在任意文件夹中鼠标右键即可出现Cmder Here**：
   - 或者在开始菜单下输入cmder搜索即可出现Cmder。

## 使用与Linux命令
Cmder支持大部分的Linux命令，如grep、curl、vim、grep、tar、unzip、ssh、ls、bash、perl等。

## 解决问题-中文未正常显示问题（乱码）
解决方法：
1. 窗口空白处右键或者窗口右下角“更多”按钮——>setting——>startup——>Environments中添加以下两行：
   ```
   set LANG=zh_CN.UTF-8
   set LC_ALL=zh_CN.utf8
   ```
2. 保存设置后，重启Cmder即可。

## 下载链接

[Cmder简介及安装使用](https://pan.quark.cn/s/11580a3ee60a)