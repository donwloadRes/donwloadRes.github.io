---
layout: post
title: "Nginx SSL使用自制证书"
date:   2020-06-08
tags: [证书,Nginx,ssl,server,SSL]
comments: true
author: admin
---
# Nginx SSL使用自制证书

本文介绍了如何在Nginx服务器中使用自制的SSL证书来配置HTTPS。通过生成JKS格式的证书并将其转换为PEM格式，以适应Nginx的配置需求。

## 1. 生成证书

首先，使用`keytool`工具生成JKS格式的证书。以下是生成证书的命令示例：

```bash
keytool -genkey -v -alias <Alias别名> -keyalg RSA -keystore <KeyStore文件> -validity <有效期>
```

例如：

```bash
keytool -genkey -v -alias nginx -keyalg RSA -keystore nginx.keystore -validity 36500
```

## 2. 转换证书

由于Nginx使用PEM格式的证书，因此需要将生成的JKS格式证书转换为PEM格式。可以使用`jks2pfx`工具进行转换。以下是转换命令示例：

```bash
JKS2PFX <KeyStore文件> <KeyStore密码> <Alias别名> <导出文件名>
```

例如：

```bash
JKS2PFX ssl/nginx.keystore 123456 nginx exportfile
```

## 3. 使用证书

在Nginx的配置文件中添加SSL证书。将生成的证书文件拷贝到Nginx的配置目录下，并在配置文件中添加以下内容：

```nginx
server {
    listen 443 ssl;
    server_name localhost;
    ssl_certificate exportfile.crt;
    ssl_certificate_key exportfile.key;
    ssl_session_cache shared:SSL:10m;
    ssl_session_timeout 10m;
    ssl_ciphers HIGH:!aNULL:!MD5;
    ssl_prefer_server_ciphers on;

    location / {
        alias D:/website/dist/;
    }
}
```

## 4. 验证

配置完成后，重启Nginx服务并验证SSL证书是否正确配置。访问网站时，浏览器应显示安全连接。

## 5. 处理缺少key的情况

如果提供的证书中缺少私钥（key），可以使用`openssl`工具从pfx文件中提取key和证书。以下是提取命令示例：

```bash
openssl pkcs12 -in xxx.pfx -nodes -out xxx.key
openssl pkcs12 -in xxx.pfx -nodes -out server.pem
openssl rsa -in server.pem -out server.key
openssl x509 -in server.pem -out server.crt
```

通过以上步骤，您可以在Nginx中成功配置自制的SSL证书，实现HTTPS加密通信。

## 下载链接

[NginxSSL使用自制证书](https://pan.quark.cn/s/7dc134330766)