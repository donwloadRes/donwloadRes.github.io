---
layout: post
title: "通过JavaScript制作一个简单的登录功能"
date:   2020-05-01
tags: [div,class,span,密码,用户名]
comments: true
author: admin
---
# 通过JavaScript制作一个简单的登录功能

本仓库提供了一个使用JavaScript制作的简单登录功能的资源文件。该功能包括一个基本的HTML页面和相应的JavaScript代码，用于实现用户登录的验证。

## 功能描述

- **HTML页面**：包含用户名和密码的输入框，以及一个登录按钮。
- **JavaScript代码**：处理用户输入的用户名和密码，并进行简单的验证。如果用户名和密码匹配预设值，则跳转到指定页面；否则，提示用户账号或密码错误。

## 使用方法

1. 下载本仓库的资源文件。
2. 打开HTML文件，即可看到登录页面。
3. 输入用户名和密码进行测试。

## 示例代码

以下是HTML页面的部分代码示例：

```html
<div class="box">
  <div class="loginBox">
    <div class="textBox">
      <span>登录</span>
      <span>Sign in</span>
    </div>
    <div class="inpBox">
      <img src="/img/user.png" alt="">
      <input id="userName" type="text" placeholder="请输入用户名">
    </div>
    <div class="inpBox">
      <img src="/img/password.png" alt="">
      <input id="passwordVal" type="password" placeholder="请输入密码">
    </div>
    <div class="textBox2">
      <span>验证码登录</span>
      <span>忘记密码</span>
    </div>
    <div class="btnBox" onclick="loginClick()">登 录</div>
    <div class="btnBox2">立即注册</div>
  </div>
  <div class="textBox3">
    为了您更好的使用<br/> &emsp;&emsp;我们将不懈努力
  </div>
</div>
```

以下是JavaScript代码的部分示例：

```javascript
function loginClick() {
  // 获取用户名
  var userName = document.getElementById('userName').value;
  // 获取密码
  var passwordVal = document.getElementById('passwordVal').value;
  // 如果用户名等于tydj并且密码等于123456则跳转页面，否则提示账号或密码错误
  if (userName === 'tydj' && passwordVal === "123456") {
    window.location.href = '/index.html';
  } else {
    alert('账号或密码错误');
  }
}
```

## 注意事项

- 该示例代码仅为简单演示，实际应用中应结合后端进行更复杂的验证和处理。
- 请根据实际需求修改和扩展代码。

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个简单的登录功能示例。

## 下载链接

[通过JavaScript制作一个简单的登录功能](https://pan.quark.cn/s/eaa761411603)