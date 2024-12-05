---
layout: post
title: "用JavaScript实现登录注册界面跳转"
date:   2020-05-21
tags: [JavaScript,界面,跳转,登录,示例]
comments: true
author: admin
---
# 用JavaScript实现登录注册界面跳转

本资源文件提供了一个用JavaScript实现的登录注册界面跳转的示例代码。通过这个示例，你可以学习如何使用JavaScript来控制页面的显示和隐藏，实现登录和注册界面的切换。

## 功能介绍

- **界面跳转**：通过JavaScript函数`TurnToLogin`和`TurnToRegister`，实现登录和注册界面的切换。
- **显示与隐藏**：通过修改HTML元素的`display`属性，控制登录和注册界面的显示与隐藏。

## 使用方法

1. **下载资源文件**：下载本仓库中的资源文件，解压后可以看到包含HTML、CSS和JavaScript的代码文件。
2. **打开HTML文件**：使用浏览器打开`index.html`文件，即可看到登录和注册界面的切换效果。
3. **查看代码**：查看`script.js`文件中的JavaScript代码，了解如何通过JavaScript控制页面元素的显示和隐藏。

## 代码示例

以下是核心JavaScript代码示例：

```javascript
var TurnToLogin = () => {
    document.getElementById('form_login_div').style.display = "block";
    document.getElementById('form_register_div').style.display = "none";
}

var TurnToRegister = () => {
    document.getElementById('form_register_div').style.display = "block";
    document.getElementById('form_login_div').style.display = "none";
}
```

## 注意事项

- 本示例代码仅实现了前端的界面跳转功能，不涉及后端的用户数据处理。
- 你可以根据需要扩展代码，添加用户数据的验证和存储功能。

通过这个示例，你可以快速上手使用JavaScript实现简单的登录注册界面跳转功能。

## 下载链接

[用JavaScript实现登录注册界面跳转](https://pan.quark.cn/s/1e3dc24cd1fc)