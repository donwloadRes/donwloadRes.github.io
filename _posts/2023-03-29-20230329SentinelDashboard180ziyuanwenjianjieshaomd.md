---
layout: post
title: "Sentinel Dashboard 180 资源文件介绍"
date:   2020-06-25
tags: [sentinel,1.8,jar,控制面板,文件]
comments: true
author: admin
---
# Sentinel Dashboard 1.8.0 资源文件介绍

## 概述

本仓库提供了一个名为 `sentinel-dashboard-1.8.0.jar` 的资源文件，该文件是 Sentinel 与 Spring Cloud Alibaba 整合的控制面板。通过该控制面板，您可以方便地管理和监控 Spring Cloud 微服务中的流量规则。

## 功能特点

- **直接运行**：该 JAR 文件可以直接运行，无需额外配置。
- **默认端口**：默认启动端口为 `8080`。
- **可视化界面**：启动后，打开浏览器输入 `localhost:8080` 即可访问 Sentinel 控制页面。
- **默认用户名和密码**：用户名和密码均为 `sentinel`。
- **流量规则管理**：通过控制面板，您可以轻松设定接口的流量规则，包括流控规则、降级规则等。

## 使用说明

1. **下载资源文件**：
   - 从本仓库下载 `sentinel-dashboard-1.8.0.jar` 文件。

2. **启动控制面板**：
   - 在命令行中执行以下命令启动控制面板：
     ```bash
     java -jar sentinel-dashboard-1.8.0.jar
     ```

3. **访问控制页面**：
   - 启动后，打开浏览器并访问 `http://localhost:8080`。
   - 使用默认用户名 `sentinel` 和密码 `sentinel` 登录。

4. **配置流量规则**：
   - 登录后，您可以通过可视化界面配置和管理接口的流量规则，包括流控、降级等。

## 注意事项

- 请确保您的系统已安装 Java 运行环境（JRE）。
- 如果您需要修改默认端口或其他配置，可以通过命令行参数进行调整。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交 Issue 或 Pull Request。

---

希望这个 `README.md` 文件能够帮助您更好地理解和使用 `sentinel-dashboard-1.8.0.jar` 资源文件。

## 下载链接

[SentinelDashboard1.8.0资源文件介绍](https://pan.quark.cn/s/391563aa3a09)