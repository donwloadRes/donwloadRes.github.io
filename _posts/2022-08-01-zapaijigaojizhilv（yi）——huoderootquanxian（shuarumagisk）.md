---
layout: post
title: "杂牌机搞机之旅（一）——获得root权限（刷入magisk）"
date:   2024-11-14
tags: [boot,Magisk,img,root,fastboot]
comments: true
author: admin
---
# 杂牌机搞机之旅（一）——获得root权限（刷入magisk）

## 简介
本资源文件旨在帮助用户在杂牌安卓手机上获得root权限，通过刷入Magisk来实现。Magisk是一款强大的工具，能够帮助用户在不修改系统分区的情况下获得root权限，同时还能隐藏root状态，避免某些应用检测到设备已被root。

## 适用条件
- **硬件要求**：安卓手机一部，Android版本需为Android 5.0以上。
- **软件要求**：当前手机对应的线刷包Rom、dev check、Magisk Manager。

## 操作步骤
1. **查看手机是否符合条件**：使用dev check查看手机的Android版本是否为5.0+，并确认是否需要解锁BootLoader（一般杂牌机不需要）。
2. **提取官方线刷包的boot.img**：将rom包中的boot.img提取出来，rom包其实是一个压缩包，解压缩后即可看到boot.img。
3. **获得修补好的boot.img**：安装Magisk Manager 7.0版本，将官方的boot.img放在手机中备用。使用Magisk Manager进行boot修补操作，生成的修补boot.img会放在Download文件夹下，将其传到电脑上。
4. **使用adb命令进入fastboot模式**：通过adb命令进入fastboot模式，手机屏幕会有显示fastboot的提示。
5. **使用fastboot命令刷入boot.img**：输入fastboot flash boot [boot.img路径]命令，刷入成功后输入fastboot reboot重启手机。
6. **验证Magisk安装成功**：打开Magisk Manager，确认Magisk安装成功并获得root权限。

## 注意事项
- 刷机有风险，操作前请备份重要数据。
- 确保手机电量充足，避免在操作过程中因电量不足导致中断。
- 操作过程中如遇到问题，请参考相关教程或寻求专业人士帮助。

## 资源文件内容
- 包含Magisk Manager 7.0版本安装包。
- 包含adb工具及fastboot工具。
- 包含官方线刷包的boot.img文件。

通过本资源文件，您可以轻松在杂牌安卓手机上获得root权限，享受更多自定义和优化手机的乐趣。

## 下载链接

[杂牌机搞机之旅一获得root权限刷入magisk分享](https://pan.quark.cn/s/16c47556183c)