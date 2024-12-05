---
layout: post
title: "基于实战渗透中用到的BurpSuite插件"
date:   2023-11-18
tags: [插件,BurpSuite,渗透,漏洞,页面]
comments: true
author: admin
---
# 基于实战渗透中用到的BurpSuite插件

本文介绍了在实战渗透测试中常用的BurpSuite插件，这些插件能够极大地提升渗透测试的效率和准确性。以下是几款常用的BurpSuite插件及其功能介绍：

## 1. Shiro被动检测插件
该插件用于被动检测Shiro框架中的漏洞。安装后，BurpSuite会自动检测访问的页面，并在发现漏洞时在Target页面中显示。

## 2. Fastjson漏洞被动检测插件
该插件用于被动检测Fastjson框架中的漏洞。与Shiro插件类似，它会在发现漏洞时在Target页面中显示。

## 3. Struts2漏洞检测插件
该插件提供了两个版本：
- **主动扫描版本**：用于主动扫描Struts2框架中的漏洞，并显示对应的CVE编号。
- **被动扫描版本**：自动检测URL后缀为`.do`和`.action`的数据包，发现漏洞时在Target和插件页面中显示为True。

## 4. 敏感信息收集工具 - HaE
HaE是一款基于BurpSuite插件JavaAPI开发的请求高亮标记与信息提取工具。用户可以通过自定义正则表达式匹配响应报文或请求报文，并决定是否需要高亮标记或信息提取。

## 5. 403Bypasser插件
该插件用于绕过403受限目录。通过PassiveScan功能，自动扫描每个403请求，帮助用户绕过访问限制。

## 6. 验证码识别插件 - captcha-killer-modified
该插件用于识别验证码。用户需要先启动codereg服务，然后抓取验证码请求包并发送给captcha-killer-modified进行识别。识别结果可以在插件中查看，并可配合Intruder模块进行爆破。

这些插件在实战渗透测试中非常有用，能够帮助安全研究人员和渗透测试员更加高效地完成任务。希望这些插件能够为您的渗透测试工作带来便利。

## 下载链接

[基于实战渗透中用到的BurpSuite插件](https://pan.quark.cn/s/3d333fd7252f)