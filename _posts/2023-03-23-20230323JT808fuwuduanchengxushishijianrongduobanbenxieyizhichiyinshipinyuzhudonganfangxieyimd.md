---
layout: post
title: "JT808 服务端程序实时兼容多版本协议支持音视频与主动安防协议"
date:   2021-12-27
tags: [协议,JT808,jt808,server,Web]
comments: true
author: admin
---
# JT808 服务端程序：实时兼容多版本协议，支持音视频与主动安防协议

## 项目介绍

`jt808-server` 是一个基于 Netty 实现的 JT808 部标协议服务端程序，旨在提供一个简洁、易用且功能强大的开发框架。该项目不仅实现了 JT808 协议的消息处理与编码解码，还集成了 SpringBoot 和 MyBatis，提供了数据入库和 Web 接口服务。协议部分不依赖 Spring，可以独立运行，甚至支持 Android 客户端。

## 主要特性

- **代码精简**：代码足够精简，便于二次开发和定制。
- **设计理念**：致敬 Spring 和 Hibernate 的设计理念，熟悉 Web 开发的同学可以快速上手。
- **注解驱动**：使用注解描述协议，告别繁琐的封包和解包过程。
- **多版本兼容**：实时兼容 JT808 2011、2013、2019 版本协议，支持分包请求。
- **协议支持**：支持 T/JSATL12 苏标主动安防协议和 JT/T1078 音视频协议（仅信令部分，流媒体服务需自行搭建）。
- **异步处理**：支持异步批量处理，显著提升 MySQL 入库性能。
- **报文解释器**：提供报文解释器，帮助分析编码解码过程，不再抓瞎。
- **测试覆盖**：全覆盖的测试用例，确保代码的稳定性和可靠性。

## 快速开始

### 环境要求

- JDK 1.8 或更高版本
- Maven 3.x
- MySQL 5.7 或更高版本

### 安装与运行

1. **克隆仓库**：
   ```bash
   git clone https://github.com/your-repo/jt808-server.git
   ```

2. **构建项目**：
   ```bash
   cd jt808-server
   mvn clean install
   ```

3. **配置数据库**：
   在 `src/main/resources` 目录下找到 `application.yml` 文件，配置数据库连接信息。

4. **启动服务**：
   ```bash
   java -jar target/jt808-server.jar
   ```

### 使用说明

- **协议配置**：通过注解配置协议，具体参考项目中的示例代码。
- **Web 接口**：项目集成了 SpringBoot，提供了基本的 Web 接口服务，可以通过浏览器或 Postman 进行测试。
- **报文解释器**：在 `src/main/resources` 目录下找到 `message-parser.yml` 文件，配置报文解释器，帮助分析编码解码过程。

## 贡献

欢迎提交 Issue 和 Pull Request。我们鼓励社区贡献，共同完善这个项目。

## 许可证

本项目采用 [MIT 许可证](LICENSE)。

## 下载链接

[JT808服务端程序实时兼容多版本协议支持音视频与主动安防协议](https://pan.quark.cn/s/04f5e86ce44a)