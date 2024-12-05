---
layout: post
title: "通过IPv6实现外网访问群晖701系统"
date:   2021-04-19
tags: [IPv6,域名,NAS,aliddns,sh]
comments: true
author: admin
---
# 通过IPv6实现外网访问群晖7.0.1系统

## 简介

本文详细介绍了如何在IPv4资源有限的情况下，利用IPv6访问家庭局域网中的NAS设备。通过以下步骤，您可以轻松实现外网访问群晖7.0.1系统，无需担心动态IP地址的变化。

## 准备工作

### 1. 检查家庭宽带是否支持IPv6

首先，打开浏览器，输入网址 `https://www.test-ipv6.com/`。如果页面显示您的家庭宽带支持IPv6，则可以继续下一步。如果不支持，请检查路由器或光猫是否开启了IPv6功能，必要时联系宽带维修师傅进行检查。

### 2. 准备域名

推荐在阿里云购买并注册一个域名。点击域名注册进行跳转，选择一个适合的域名并完成注册。

### 3. 下载 aliddns.sh 文件

下载 `aliddns.sh` 文件，该文件的作用是当NAS的IPv6地址重新分配之后，通知阿里云重新解析域名，将新的IPv6地址与域名重新绑定在一起。

## 实际操作

### 1. 配置 aliddns.sh 文件

在 `aliddns.sh` 文件中配置以下参数：

- `AccessKeyId` 和 `Access Key Secret`：在阿里云中获取。
- `aliddnsipv6_name1`：自定义一个名字，需要符合域名规范。
- `aliddnsipv6_domain`：填写自己注册的域名。
- `aliddnsipv6_ttl`：设置TTL值，建议设置为600。

### 2. 配置网卡名称

将 `aliddns.sh` 文件中第20行的 `eth0` 更改成自己的网卡名称。可以通过在NAS上执行 `ipconfig` 命令获取网卡配置，找到拥有 `inet6 addr: 240e:331:xxxx:xxxx:xxxx:xxxx:fe12:3466/64 Scope:Global` 的网卡名称。

### 3. 域名解析

进入阿里云控制台，解析域名，添加记录：

- 记录类型：AAAA
- 主机记录：与 `aliddns.sh` 文件中的 `aliddnsipv6_name1` 值一致
- 记录值：NAS系统的IPv6地址
- TTL：10分钟

### 4. NAS系统添加任务计划

在NAS的控制面板中，进入任务计划，新增一个计划任务，设置每天每10分钟执行一次 `aliddns.sh` 文件。执行一次该任务，等待阿里云解析完成，即可通过IPv6访问NAS。

## 其他

通过以上步骤，您可以成功实现通过IPv6访问群晖7.0.1系统。如果遇到任何问题，可以参考本文中的详细步骤进行排查。

## 下载链接

[通过IPv6实现外网访问群晖7.0.1系统分享](https://pan.quark.cn/s/c22efa56cccb)