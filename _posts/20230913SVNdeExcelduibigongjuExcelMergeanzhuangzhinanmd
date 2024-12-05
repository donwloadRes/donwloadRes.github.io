---
layout: post
title: "SVN的Excel对比工具ExcelMerge安装指南"
date:   2023-05-15
tags: [ExcelMerge,SVN,安装,Excel,文件]
comments: true
author: admin
---
# SVN的Excel对比工具ExcelMerge安装指南

## 简介
ExcelMerge是一个在Windows平台下比对Excel文件的工具，特别适用于需要比对多个Sheet的Excel文件。配合SVN使用，可以方便地查看策划的数值表变化。本资源文件提供了ExcelMerge的安装步骤和集成到SVN中的详细说明。

## 安装步骤

### 1. 下载并安装ExcelMerge
- 下载地址：百度网盘（提取码：1996）
- 点击镜像文件进行安装，安装过程中无脑Next即可。

### 2. 集成到SVN中
- 配置SVN的Diff Viewer
- 在最后的弹框中填入内容：`"C:\Program Files (x86)\ExcelMerge\ExcelMerge.GUI.exe" -s %base -d %mine`
  - 注意：如果安装过程中不是默认的安装位置，请做对应的修改。

### 3. 配置完成后
- 打开「svn log」，随意双击log中出现的excel文件即可对比历史版本中的差异。

## 集成到Fork中
- 启动Fork，并打开File（文件） -> Preference（首选项）
- 选择Integration（集成）
- 配置External Diff Tool
  - 路径选择到刚才安装的目录，如果时默认安装使用目录：`C:\Program Files (x86)\ExcelMerge\ExcelMerge.GUI.exe`
  - 参数中填写：`-s $REMOTE -d $LOCAL`

## 使用说明
- 安装完成后，可以在SVN中直接对比Excel文件的差异，方便查看策划的数值表变化。

## 注意事项
- 确保安装路径正确，如果安装路径不是默认路径，请在配置时进行相应修改。
- 使用时，只需双击SVN提交中的对应EXCEL文档或双击日志中的EXCEL即可进行对比。

## 作者
- 夏日微风5

## 版权声明
- 本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[SVN的Excel对比工具ExcelMerge安装指南分享](https://pan.quark.cn/s/2a16407b254a)