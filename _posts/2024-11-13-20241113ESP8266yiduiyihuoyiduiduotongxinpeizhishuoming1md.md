---
layout: post
title: "ESP8266一对一或一对多通信配置说明1"
date:   2023-07-18
tags: [模块,发送数据,TCP,标号,ESP8266]
comments: true
author: admin
---
# ESP8266一对一或一对多通信配置说明1

## 资源文件描述

在本例中，模块2与模块1的TCP标号为0，因此，模块1向模块2发送数据时，指令为`AT+CIPSEND=05`。其中，等号后的0为TCP的标号，5为发送数据的字节数。

## 使用说明

1. **TCP标号**：模块1与模块2之间的TCP连接标号为0。
2. **发送数据指令**：模块1向模块2发送数据时，使用指令`AT+CIPSEND=05`，其中0表示TCP标号，5表示发送数据的字节数。

## 注意事项

- 确保模块1和模块2之间的TCP连接已经建立。
- 发送数据时，确保指令中的字节数与实际发送的数据长度一致。

通过本说明，您可以轻松配置ESP8266模块进行一对一或一对多的通信。

## 下载链接

[ESP8266一对一或一对多通信配置说明1.docx](https://pan.quark.cn/s/337649a7cc6a)