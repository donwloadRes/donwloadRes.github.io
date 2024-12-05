---
layout: post
title: "MAC M1版IDEA热部署JRebel 使用指南"
date:   2020-12-15
tags: [JRebel,IDEA,插件,激活,M1]
comments: true
author: admin
---
# MAC M1版IDEA热部署JRebel 使用指南

## 概述

本文档旨在提供详尽的指导，帮助您在配备M1芯片的Mac设备上，顺利配置IntelliJ IDEA的JRebel插件以实现热部署功能。JRebel是一款高效的开发工具，极大加速Java应用的开发流程，允许开发者在无需重启应用的情况下即时看到代码更改的效果。

## 步骤概览

1. **安装JRebel插件**
   - 在IntelliJ IDEA中，访问插件市场，搜索“JRebel”并安装。
   - 或者，下载ZIP文件，并通过IDE的设置界面手动安装。

2. **下载激活工具**
   - 对于M1用户，建议从GitHub或指定百度网盘链接（提取码: ukhh）下载适合Mac的激活工具(`ReverseProxy_darwin_amd64`)。
   - 注意：使用Safari下载，避免Chrome可能会移除`.dmg`扩展名的问题。

3. **配置激活**
   - 在终端中，给予激活工具执行权限：`chmod 777 '文件路径'`，然后执行文件：`$bash '文件路径'`。
   - 通过浏览器生成GUID并激活JRebel插件，在插件设置中填入相应信息，连接至本地代理服务激活。

4. **IDEA配置**
   - 根据IDE版本，确保已开启内置的编译功能。
   - 对于Spring Boot项目，可在`pom.xml`中加入`spring-boot-devtools`作为热部署的依赖。

5. **离线使用**
   - 若需离线使用，进入JRebel设置，点击“Work offline”，插件将在设定的期限内有效，到期重复激活过程即可。

## 注意事项

- 确保IDEA版本与JRebel插件兼容。
- 激活时，注意选择正确的激活方式，特别是最新版本的IDEA可能需要特别的激活策略。
- 遇到任何问题，检查IDEA的版本、插件版本及系统兼容性。

通过遵循上述步骤，您的MAC M1设备上的IntelliJ IDEA将能够利用JRebel的强大热部署能力，大大提高开发效率。记得适时查阅最新的官方指南或社区文章，以获取最准确的更新信息和技术支持。

## 下载链接

[MACM1版IDEA热部署JRebel使用指南](https://pan.quark.cn/s/8785f95dac6a)