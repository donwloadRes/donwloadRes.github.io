---
layout: post
title: "MDK Keil 自动补全功能设置问题解决方案"
date:   2022-09-19
tags: [Keil,补全,编程,自动,文件夹]
comments: true
author: admin
---
# MDK Keil 自动补全功能设置问题解决方案

## 简介

在使用MDK Keil进行编程时，自动补全功能是一个非常实用的工具，可以大大提高编程效率。然而，有些用户可能会遇到无法设置自动补全功能的问题，具体表现为在设置界面中，Text Completion选项一片空白。本文将详细介绍如何解决这一问题。

## 问题描述

在Keil编程时，有些变量名会很长，如果手打的话很浪费时间。Keil 4.7以上的版本就更新了自动补全功能，也就是输入变量前几个字母，自动联想整个变量。但是，当我们进入Edit-Configuration-Text Completion时，发现本来可以设置的自动补全功能是空白一片，而我们的Keil确实是高版本的Keil。

## 解决方案

### 1. 避免使用汉化版Keil

首先，汉化版的Keil是没有这个功能的，所以最好不用汉化版的Keil。其实在编程当中，我们需要用到的单词也不多，所以用英文版的更好，不会出现一些奇奇怪怪的bug。

### 2. 替换相关文件

不需要重新安装Keil，只需要替换一些文件即可。具体步骤如下：

1. 下载Keil安装包。
2. 解压下载之后的压缩包，然后进入文件夹。
3. 把文件夹里面的【mdk518.exe】解压在当前文件夹，然后就会出现很多文件，我们进入【UV4】文件夹。
4. 把【UV4】文件夹里面的【UV4.exe】文件进行复制。
5. 右键点击我们本来已经安装好的Keil，点击【打开文件所在的位置】，然后把我们刚才复制的文件粘贴在里面，选择替换。

### 3. 重新打开软件

重新打开软件后，我们会发现本来空白的地方已经有了。我们可以看到输入3个字母后，Keil就会自动产生联想，上下方向键选择，Enter/Tab键进行确认，这样就可以快速进行编程了。

## 总结

通过以上步骤，您可以成功解决MDK Keil自动补全功能设置空白的问题，提高编程效率。希望本文对您有所帮助！

## 下载链接

[MDKKeil自动补全功能设置问题解决方案](https://pan.quark.cn/s/c2011cb1da4e)