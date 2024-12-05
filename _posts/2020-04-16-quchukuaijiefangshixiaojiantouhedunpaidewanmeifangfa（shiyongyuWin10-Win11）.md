---
layout: post
title: "去除快捷方式小箭头和盾牌的完美方法（适用于Win10-Win11）"
date:   2024-05-08
tags: [快捷方式,Windows,图标,Shell,Icons]
comments: true
author: admin
---
# 去除快捷方式小箭头和盾牌的完美方法（适用于Win10/Win11）

## 简介
本资源文件提供了一种“比较完美”的方法，用于去除Windows 10和Windows 11系统中快捷方式图标上的小箭头和盾牌。通过这种方法，您可以自定义图标，使其更加美观。

## 适用系统
- Windows 10
- Windows 11

## 实现效果
- 去除快捷方式图标上的小箭头
- 去除快捷方式图标上的盾牌

## 替换方法
1. 将 `BlankImageres.dll.mun` 文件放到 `System32` 文件夹下，也可以自己指定文件夹，后面的数值数据就填写自己的文件路径，最好是放在不易改变的地方。
2. 在“注册表编辑器”中，按照以下路径找到对应项：
   ```
   HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Icons
   ```
   如果在 `Explorer` 下面没有“Shell Icons”这一项，可以直接在 `Explorer` 项上点击鼠标右键，选择“新建”→“项”，然后把项的名字重命名为“Shell Icons”。
3. 选中“Shell Icons”，在右侧窗口中新建两条字符串值：
   ```
   C:\Windows\System32\BlankImageres.dll.mun
   ```
4. 然后重启资源管理器即可。如果没有生效，可以去删除图标缓存文件 `C:\用户\AppData\Local\iconcache.db`，然后再重启资源管理器。

## 恢复方法
恢复快捷方式小箭头和盾牌的方法：
1. 把这两条字符串值删除，或者直接删除 `Shell Icons` 这个项。
2. 然后重启资源管理器。如果没有生效，可以去删除图标缓存文件 `C:\用户\AppData\Local\iconcache.db`，然后再重启资源管理器。

## 注意事项
- 更改注册表是一项风险较高的操作，请谨慎操作，并备份注册表以防不测。
- 本方法适用于大多数用户，但具体效果可能因系统配置不同而有所差异。

## 作者
- 作者：vickers9585
- 文章来源：CSDN博客

## 版权声明
本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[去除快捷方式小箭头和盾牌的完美方法适用于Win10Win11](https://pan.quark.cn/s/d1a7b03e9e35)