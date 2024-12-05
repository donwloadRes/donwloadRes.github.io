---
layout: post
title: "U盘安装Mac High Sierra指南"
date:   2021-01-02
tags: [U盘,Mac,Sierra,High,启动盘]
comments: true
author: admin
---
# U盘安装Mac High Sierra指南

本资源文件提供了详细的步骤，帮助你在Mac系统中制作U盘启动盘，以便安装Mac High Sierra操作系统。以下是制作U盘启动盘的步骤：

## 准备工作
1. **U盘**：准备一个8GB或更大容量的U盘，并备份好U盘中的所有数据。
2. **Mac系统**：确保你当前使用的是Mac系统。

## 制作U盘启动盘步骤

### 1. 下载macOS High Sierra
- 从App Store下载macOS High Sierra安装程序。

### 2. 备份U盘数据
- 将U盘插入Mac电脑，并备份U盘中的所有数据。

### 3. 格式化U盘
- 打开“应用程序 -> 实用工具 -> 磁盘工具”。
- 选择U盘的父节点，点击“抹掉”。
- 选择“Mac OS扩展（日志式）”和“GUID分区图”，点击“抹掉”。

### 4. 制作系统启动盘
- 打开“应用程序 -> 实用工具 -> 终端”。
- 输入以下命令（将`/Volumes/Sierra`替换为你的U盘名称）：
  ```
  sudo /Applications/Install\ macOS\ High\ Sierra.app/Contents/Resources/createinstallmedia --volume /Volumes/Sierra --applicationpath /Applications/Install\ macOS\ High\ Sierra.app --nointeraction
  ```
- 回车后输入电脑登录密码，开始制作。当看到“Done”提示时，制作成功。

### 5. 使用U盘安装系统
- 备份好Mac电脑中的资料。
- 重启系统，同时按下`command + R`不放，直到出现启动管理器。
- 选择磁盘工具抹掉原有系统，再回到启动管理器页面。
- 插入U盘，关闭该界面，按提示点击按钮，选择安装系统。
- 回到上一界面后，选择“重新安装OS X”，之后按照提示进行下一步操作。

通过以上步骤，你就可以成功制作并使用U盘启动盘来安装Mac High Sierra操作系统。

## 下载链接

[U盘安装MacHighSierra指南分享](https://pan.quark.cn/s/0fba01f121d8)