---
layout: post
title: "模型训练完成发送消息到手机安卓iOS"
date:   2024-09-22
tags: [ntfy,安卓,模型,训练,iOS]
comments: true
author: admin
---
# 模型训练完成发送消息到手机(安卓/iOS)

## 简介
在机器学习模型的训练过程中，训练时间可能长达数小时甚至数天。为了在模型训练完成后及时收到通知，本文介绍了一种使用ntfy服务的方法，通过简单的配置和代码修改，实现模型训练完成后自动向手机发送通知。

## 实现步骤

### 1. 下载ntfy应用
- **iOS/iPad OS**: 在App Store中搜索并下载“ntfy”应用。
- **安卓/Android**: 在Google Play中搜索并下载“ntfy”应用。如果无法访问Google Play，可以使用提供的网盘链接下载apk文件进行安装。

### 2. 自定义话题(Topic)
打开ntfy应用，点击右上角的加号，自定义一个话题。话题名称可以使用字母、数字或下划线组合，建议设置复杂一些以避免与其他用户的话题冲突。

### 3. 测试推送
创建一个Python文件，内容如下：
```python
import requests
requests.post("https://ntfy.sh/<你的话题>", data="Test from python code", encode(encoding='utf-8'))
```
如果没有requests包，需要先安装该包。执行该Python文件后，手机端会收到一个测试消息。

### 4. 在模型训练代码中添加推送代码
在模型的主调用程序中，添加上述推送代码，位置设置在模型训练结束后。

## 进阶使用
ntfy不仅支持Python，还可以在命令行、Go、PHP等编程环境中使用。可以参考官方文档了解更多使用方法。

## 注意事项
ntfy的消息分为五个等级，默认等级为3，在安卓手机上可能不会弹窗提醒。如果需要弹窗提醒，需要在通知设置中修改通知类型，赋予对应等级的消息“悬浮通知权限”。

## 下载链接

[模型训练完成发送消息到手机安卓iOS](https://pan.quark.cn/s/c091d1173454)