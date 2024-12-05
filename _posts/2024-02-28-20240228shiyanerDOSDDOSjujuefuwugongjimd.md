---
layout: post
title: "实验二DOSDDOS拒绝服务攻击"
date:   2022-01-22
tags: [攻击,拒绝服务,Wireshark,DDoS,--]
comments: true
author: admin
---
# 实验二：DOS/DDOS拒绝服务攻击

## 实验简介
本实验旨在帮助学生深入了解DOS（拒绝服务）和DDoS（分布式拒绝服务）攻击的形成原因、攻击方式及其危害。通过实际操作，学生将学会使用Kali Linux中的Wireshark抓包工具和相关命令，观察并分析攻击行为特征，从而更好地理解如何防御此类攻击。

## 预备知识
在进行本实验之前，学生需要具备以下相关知识：
1. **DoS简介**：了解拒绝服务攻击的基本概念和早期攻击方式。
2. **DDoS简介**：理解分布式拒绝服务攻击的原理和目的。
3. **DDoS危害**：认识DDoS攻击对网络和服务器的具体影响。

## 实验目的
1. 让学生充分了解DOS/DDOS拒绝服务攻击的形成原因。
2. 学会使用Kali Linux中的Wireshark和相关命令。

## 实验环境
- **Kali Linux**：用于执行攻击命令和抓包分析。
- **Win 7**：作为目标系统，用于观察攻击效果。

## 实验步骤
1. **打开Vmware，启动Kali Linux虚拟机**。
2. **进入Kali Linux虚拟机，打开Wireshark抓包软件，监听虚拟机上网网卡**。
3. **进入命令终端，运行Hping3程序**，使用以下命令进行ICMP泛洪攻击：
   ```
   sudo hping3 --icmp --rand-source --flood 目标IP
   ```
4. **Wireshark观察ICMP协议包，学习攻击行为特征**。
5. **Wireshark停止抓包，保存攻击数据包到本地**。
6. **进行UDP flood攻击**，使用以下命令：
   ```
   sudo hping3 --udp --rand-source --flood 目标IP
   ```
7. **Wireshark观察UDP协议包，学习攻击行为特征**。

## 实验总结
通过本实验，学生将能够：
1. 理解DOS/DDoS攻击的基本原理和实施方法。
2. 掌握使用Wireshark抓包工具分析网络攻击行为。
3. 认识到DDoS攻击对网络和服务器的严重危害，增强网络安全意识。

## 注意事项
1. 本实验仅供学习和研究使用，请勿用于非法目的。
2. 在进行实验时，务必确保所有操作在合法和授权的环境中进行。

## 下载链接

[实验二DOSDDOS拒绝服务攻击分享](https://pan.quark.cn/s/0363fe9a7cad)