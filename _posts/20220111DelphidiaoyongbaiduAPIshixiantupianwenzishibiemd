---
layout: post
title: "Delphi调用百度API实现图片文字识别"
date:   2023-02-24
tags: [Delphi,编码,图片,识别,乱码]
comments: true
author: admin
---
# Delphi调用百度API实现图片文字识别

本资源文件提供了一个用Delphi 2010编写的示例代码，展示了如何调用百度API实现图片文字识别功能。在开发过程中，我们遇到了一些常见问题，并提供了相应的解决方案，供需要的朋友参考。

## 主要内容

### 1. SSL问题
在使用Indy HTTP控件进行SSL通信时，需要添加`IdSSLIOHandlerSocketOpenSSL1`组件，并将`idhttp`的`iohandler`属性指向`IdSSLIOHandlerSocketOpenSSL1`。同时，需要将`SSLoptions`的`method`属性改为`sslvSSLv23`。此外，还需要放置两个SSL所需的DLL文件，确保Delphi 2010兼容。

### 2. 图片编码问题
在初始尝试中，我们遇到了`error_code:216201`和`error_msg:image format error`的错误。经过排查，发现是Indy控件默认会对参数进行重新编码。通过关闭`httpoptions`下的`hoforceencodeparams`属性，图片上传问题得以解决。图片需要先进行Base64编码，然后再进行URL编码。

### 3. 识别完成后的中文乱码问题
在获取识别结果时，直接使用`result:= indyhttp.post(urlimg)`方法会导致返回值被Indy再次编码，从而引发中文乱码问题。我们最终改为使用流接收返回值，并进行UTF-8解码，成功解决了乱码问题。

## 使用说明

1. 下载并导入示例代码到Delphi 2010环境中。
2. 根据上述解决方案，配置SSL相关组件和属性。
3. 确保图片编码和URL编码正确。
4. 使用流接收返回值，并进行UTF-8解码，以避免中文乱码问题。

希望本资源文件能够帮助你在Delphi中成功实现图片文字识别功能。如果有任何问题或建议，欢迎反馈。

## 下载链接

[Delphi调用百度API实现图片文字识别](https://pan.quark.cn/s/c0d7d7f8aca5)