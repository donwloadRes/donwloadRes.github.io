---
layout: post
title: "Spring Boot 323 集成 ShardingSphere 541 及动态数据源 Demo 项目"
date:   2022-01-13
tags: [数据源,Spring,Boot,ShardingSphere,动态]
comments: true
author: admin
---
# Spring Boot 3.2.3 集成 ShardingSphere 5.4.1 及动态数据源 Demo 项目

## 项目描述

本项目是一个基于 Spring Boot 3.2.3 的应用程序，集成了 ShardingSphere 5.4.1 和动态数据源功能。项目解决了 Spring Boot 与 ShardingSphere 的兼容性问题，并实现了在多个动态数据源之间切换的功能，包括 ClickHouse (CK) 和两个 MySQL 数据库。

## 主要功能

1. **兼容性解决**：解决了 Spring Boot 3.2.3 与 ShardingSphere 5.4.1 的兼容性问题，确保项目能够稳定运行。
2. **动态数据源切换**：支持在多个动态数据源之间灵活切换，包括 ClickHouse 和两个 MySQL 数据库。

## 使用说明

1. **克隆项目**：
   ```bash
   git clone https://github.com/your-repo-url.git
   ```

2. **配置数据源**：
   在 `application.yml` 或 `application.properties` 文件中配置 ClickHouse 和 MySQL 数据库的连接信息。

3. **启动项目**：
   ```bash
   mvn spring-boot:run
   ```

4. **测试动态数据源切换**：
   通过调用相应的 API 或服务方法，测试在不同数据源之间的切换功能。

## 依赖项

- Spring Boot 3.2.3
- ShardingSphere 5.4.1
- 动态数据源支持

## 贡献

欢迎大家提交 Issue 和 Pull Request，共同完善这个项目。

## 许可证

本项目采用 MIT 许可证，详情请参阅 [LICENSE](LICENSE) 文件。

## 下载链接

[SpringBoot3.2.3集成ShardingSphere5.4.1及动态数据源Demo项目](https://pan.quark.cn/s/589b41316303)