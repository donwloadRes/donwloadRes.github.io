---
layout: post
title: "IntelliJ IDEA 2017 汉化包及教程"
date:   2022-02-28
tags: [IntelliJ,IDEA,cn,resources,jar]
comments: true
author: admin
---
# IntelliJ IDEA 2017 汉化包及教程

## 简介
本仓库提供IntelliJ IDEA 2017版本的汉化包及详细汉化教程，帮助中文用户更方便地使用这款强大的开发工具。

## 汉化包内容
- `resources_cn.jar`：汉化包核心文件，包含所有界面元素的中文翻译。

## 汉化教程
### 准备工作
1. 从官网下载并安装IntelliJ IDEA 2017。
2. 下载本仓库提供的汉化包。

### 汉化步骤
#### 方法一：快捷汉化
1. 将汉化包中的`resources_cn.jar`文件复制到IntelliJ IDEA安装目录下的`lib`文件夹中。
2. 重新启动IntelliJ IDEA，界面将显示为中文。

#### 方法二：详细汉化
1. 将IntelliJ IDEA安装目录下`lib`文件夹中的`resources_en.jar`文件复制出来，并重命名为`resources_cn.jar`。
2. 双击打开`resources_cn.jar`文件（注意是打开而不是解压），将汉化包中的`zh_cn`目录下的所有文件复制并粘贴到`resources_cn.jar`中的`messages`目录中，如有重名提示，点击替换。
3. 将修改后的`resources_cn.jar`文件复制回IntelliJ IDEA安装目录下的`lib`文件夹中。
4. 重新启动IntelliJ IDEA，界面将显示为中文。

### 注意事项
- 如果汉化后出现乱码，请先删除`resources_cn.jar`，然后打开IntelliJ IDEA，在菜单上依次选择`File -> Settings -> Appearance & Behavior -> Appearance`，选中`Override default fonts by(not recommended)`，选择任意中文字体（如Microsoft YaHei）。
- 重新将`resources_cn.jar`复制到`lib`目录，再次启动IntelliJ IDEA即可正常显示中文。

## 贡献
欢迎提交问题和改进建议，帮助我们完善这个汉化包和教程。

## 许可证
本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[IntelliJIDEA2017汉化包及教程分享](https://pan.quark.cn/s/56d0915ee810)