---
layout: post
title: "微信小程序最新获取头像方法onChooseAvatar"
date:   2021-04-20
tags: [头像,获取,链接,微信,onChooseAvatar]
comments: true
author: admin
---
# 微信小程序最新获取头像方法：onChooseAvatar

## 资源描述

本文是我在学习微信小程序开发过程中，第一次撰写的资源文章。作为一名初出茅庐的小白，我采用了原生写法来实现微信小程序中获取用户头像的功能。希望通过这篇文章，能够与正在学习小程序开发的朋友们相互学习，共同进步。

### 主要内容

1. **onChooseAvatar绑定button事件**：通过`onChooseAvatar`方法绑定按钮事件，实现点击按钮获取用户头像的功能。
   - **1.1 头像临时链接的存储**：获取到的头像链接是临时的，因此我分别定义了全局变量和缓存来存储这个临时链接。后续可以将头像上传至服务器，生成永久链接，避免链接失效。
   - **1.2 自动生成头像文件名**：为了方便上传，我自动生成了头像的文件名，确保上传时图片名称的唯一性。
   - **1.3 缓存头像链接**：将获取到的头像链接存入缓存中，在“我的个人中心”页面可以同步显示用户的头像。

2. **后续计划**：
   - **2 昵称获取的方法详解**
   - **3 获取用户code、openid、session_key的方法**
   - **4 手机号获取和存入数据库方法**
   - **5 根据用户openid更新数据库里用户的昵称、手机号等信息的方法**

### 学习建议

如果你也是刚接触小程序开发的小白，欢迎关注我的后续文章。我们可以一起探讨学习中遇到的问题，共同进步。期待你的关注和支持！

---

**请继续关注我的后续文章，感谢支持！**

## 下载链接

[微信小程序最新获取头像方法onChooseAvatar](https://pan.quark.cn/s/2a36ad6ccc01)