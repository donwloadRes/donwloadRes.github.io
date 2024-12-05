---
layout: post
title: "Struts 2 全版本漏洞检测工具 18.09 过WAF版"
date:   2024-03-21
tags: [S2,漏洞,工具,Struts,检测]
comments: true
author: admin
---
# Struts 2 全版本漏洞检测工具 18.09 过WAF版

## 简介
本仓库提供了一个针对Struts 2框架的全版本漏洞检测工具，版本号为18.09，特别优化以绕过WAF（Web应用防火墙）的检测。该工具能够自动检测目标URL是否存在多种Struts 2漏洞，并提供多种功能以满足不同的检测需求。

## 功能特点
1. **自动漏洞检测**：点击“检测漏洞”按钮，工具会自动检测目标URL是否存在以下十余种Struts 2漏洞：
   - S2-001
   - S2-005
   - S2-009
   - S2-013
   - S2-016
   - S2-019
   - S2-020/021
   - S2-032
   - S2-033/037
   - DevMode
   - S2-045/046
   - S2-048
   - S2-053
   - S2-057

2. **批量验证**：工具支持批量验证功能，但为了防止滥用，批量上传功能已被永久删除，不再开发。

3. **漏洞扫描限制**：S2-020、S2-021仅提供漏洞扫描功能，因漏洞测试方法可能导致网站访问异常，本程序未提供相关测试功能。

4. **全局Cookie设置**：对于需要登录的页面，用户可以勾选“设置全局Cookie值”，并填入相应的Cookie，程序每次发包都会带上该Cookie。

5. **通用测试语句**：作者对不同的Struts 2漏洞测试语句进行了大量修改，执行命令和上传功能已经能够通用。

6. **HTTPS支持**：工具支持HTTPS协议，确保在安全环境下进行漏洞检测。

7. **多种请求方法**：支持GET、POST、UPLOAD三种请求方法，用户可以根据需要自由选择。（UPLOAD为Multi-Part方式提交）

8. **编码转换**：部分漏洞测试支持UTF-8、GB2312、GBK编码转换，确保测试结果的准确性。

9. **多线程操作**：每次操作都启用一个线程，防止界面卡死，提升用户体验。

## 使用说明
1. 下载并解压资源文件。
2. 运行工具，输入目标URL。
3. 根据需要选择相应的功能，如“检测漏洞”、“设置全局Cookie值”等。
4. 点击“开始检测”按钮，工具将自动进行漏洞检测。

## 注意事项
- 请确保在使用本工具时遵守相关法律法规，仅在授权范围内进行测试。
- 本工具仅供学习和研究使用，不得用于非法用途。

## 作者
本工具由[作者姓名]开发，如有任何问题或建议，请联系[作者联系方式]。

## 版本历史
- 18.09：初始版本，支持多种Struts 2漏洞检测，优化WAF绕过功能。

## 免责声明
本工具仅用于合法的安全测试和漏洞研究，作者不对任何非法使用本工具造成的后果负责。请用户在使用本工具时遵守相关法律法规，并获得合法授权。

## 下载链接

[Struts2全版本漏洞检测工具18.09过WAF版](https://pan.quark.cn/s/095239c5802a)