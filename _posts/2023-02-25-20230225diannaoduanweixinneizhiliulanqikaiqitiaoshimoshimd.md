---
layout: post
title: "电脑端微信内置浏览器开启调试模式"
date:   2021-08-08
tags: [微信,浏览器,内置,resources,devtools]
comments: true
author: admin
---
# 电脑端微信内置浏览器开启调试模式

本仓库提供了一个资源文件，用于在电脑端微信内置浏览器中开启调试模式。通过使用该资源文件，开发者可以在微信内置浏览器中进行调试，方便排查和解决网页相关问题。

## 使用步骤

1. **查看微信内置浏览器的版本**  
   首先，使用电脑将链接 `http://wx.gnnu.work/` 发给任意一个人，然后自己再点开这个链接，就能看到如下界面。

2. **下载devtools_resources.pak并加入到微信的内置浏览器当中**  
   复制步骤1中获得的 `--resources-dir-path` 后面的路径，并打开该文件夹，把微信版本对应的 `devtools_resources.pak` 放到该路径中。文末有下载链接。  
   再把 `devtools_resources.pak` 文件复制一份到微信的安装路径下。

3. **启动微信内置浏览器的debug**  
   在微信右键启动快捷方式->属性->目标末尾添加一个空格再添加 `-remote-debugging-port=8000`。  
   重启微信，打开青年大学习。  
   右键会发现多了三个选项，选择 `show DevTools` 就能打开控制台了。  
   发现微信内置浏览器的控制台和Chrome的控制台超级相像。  
   最后在Console下执行以下语句就能显示青年大学习播放的控件了：  
   ```javascript
   document.getElementById('Bvideo').controls = true;
   ```

## 注意事项

- 请确保微信版本与 `devtools_resources.pak` 文件版本匹配。
- 在执行调试操作时，请确保微信处于最新版本，以避免兼容性问题。

## 资源文件下载

请在仓库中下载 `devtools_resources.pak` 文件，并按照上述步骤进行操作。

---

通过以上步骤，您可以在电脑端微信内置浏览器中开启调试模式，方便进行网页开发和调试工作。

## 下载链接

[电脑端微信内置浏览器开启调试模式](https://pan.quark.cn/s/e04de193632c)