---
layout: post
title: "Coremail-0day敏感文件泄露漏洞批量检测脚本"
date:   2020-11-25
tags: [Coremail,漏洞,脚本,邮件系统,敏感]
comments: true
author: admin
---
# Coremail-0day敏感文件泄露漏洞批量检测脚本

## 简介

本仓库提供了一个针对Coremail邮件系统0day敏感文件泄露漏洞的批量检测脚本。该漏洞允许攻击者在未授权的情况下，通过远程访问URL地址获知Coremail服务器的系统配置文件，造成数据库连接参数等系统敏感配置信息泄露。

## 漏洞背景

Coremail邮件系统是国内广泛使用的电子邮件系统，拥有超过10亿终端用户。2019年5月22日，国家信息安全漏洞共享平台（CNVD）收录了由北京天融信网络安全技术有限公司报送的Coremail邮件系统信息泄露漏洞（CNVD-2019-16798）。

## 漏洞详情

该漏洞存在于Coremail邮件系统的mailsms模块中，由于参数大小写敏感存在缺陷，攻击者可以通过构造特定的URL地址，获取服务器的系统配置文件，包括文件路径、IP、端口、数据库用户、密码等敏感信息。

## 使用方法

1. 下载本仓库中的批量检测脚本。
2. 根据脚本说明进行配置和运行。
3. 脚本将自动检测目标邮件服务器是否存在该漏洞，并输出检测结果。

## 注意事项

- 请勿将本脚本用于非法用途。
- 使用前请确保已获得合法授权。
- 建议在测试环境中使用，避免对生产环境造成影响。

## 贡献

欢迎提交问题和改进建议，帮助完善本脚本。

## 许可证

本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处声明。

## 下载链接

[Coremail-0day敏感文件泄露漏洞批量检测脚本](https://pan.quark.cn/s/c4d15550a95c)