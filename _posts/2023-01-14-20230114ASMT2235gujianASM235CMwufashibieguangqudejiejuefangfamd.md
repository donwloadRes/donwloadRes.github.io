---
layout: post
title: "ASMT2235固件ASM235CM无法识别光驱的解决方法"
date:   2020-09-22
tags: [固件,光驱,识别,驱线,ASMT]
comments: true
author: admin
---
# ASMT-2235固件(ASM235CM)无法识别光驱的解决方法

## 简介
本资源文件提供了关于ASMT-2235固件（ASM235CM）无法识别光驱的解决方法。该问题通常出现在使用易驱线连接内置光驱时，电脑无法正确识别光驱设备。通过更新固件，可以有效解决这一问题。

## 问题描述
在使用ASMT-2235芯片的易驱线连接内置光驱时，可能会遇到以下问题：
- 电脑无法识别光驱设备。
- 打开光驱时电脑卡死。

## 解决方法
### 1. 下载固件及刷固件工具
- 固件文件：`171120_D1_1E_80.bin`
- 刷固件工具：`MPTool.exe`

### 2. 刷固件步骤
1. 将易驱线插到电脑上，但不要接光驱。
2. 打开刷固件工具`MPTool.exe`。
3. 识别出易驱线里的芯片。
4. 输入密码`asmedia`解锁设置。
5. 选中固件文件`171120_D1_1E_80.bin`，点击`Start`开始刷固件。
6. 等待右下角出现`PASS`提示，表示固件刷写成功。
7. 将易驱线接上光驱，检查是否成功识别。

## 注意事项
- 刷固件过程中，确保易驱线接上12V2A的电源。
- 如果识别失败，多尝试几次拔插易驱线。

## 结果验证
- 打开Windows资源管理器，查看是否出现`DVD/CD-ROM drives`。
- 或者打开设备管理器，检查是否成功识别光驱设备。

通过以上步骤，可以有效解决ASMT-2235固件无法识别光驱的问题。

## 下载链接

[ASMT-2235固件ASM235CM无法识别光驱的解决方法](https://pan.quark.cn/s/9d91a795350f)