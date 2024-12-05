---
layout: post
title: "DynamicDatasource  ShardingSphereJDBC 实现分库分表 Demo"
date:   2021-06-24
tags: [分库,数据源,分表,JDBC,切换]
comments: true
author: admin
---
# Dynamic-Datasource + ShardingSphere-JDBC 实现分库分表 Demo

## 项目描述

本项目是博客文章《dynamic-datasource+shardingsphere-jdbc实现分库分表demo》对应的示例代码。基于Spring Boot 2.7，整合了Dynamic-Datasource、ShardingSphere-JDBC以及MyBatis-Plus技术栈，实现了动态切换数据源以及对部分库表的分库分表功能。适用于老系统增加新的分库分表数据源的场景。

## 功能特点

- **动态数据源切换**：支持在运行时动态切换不同的数据源，适用于多数据源的应用场景。
- **分库分表**：通过ShardingSphere-JDBC实现对部分库表的分库分表，提升数据库的扩展性和性能。
- **MyBatis-Plus集成**：结合MyBatis-Plus，简化数据库操作，提高开发效率。

## 适用场景

本项目适用于以下场景：

- 老系统需要增加新的分库分表数据源。
- 需要动态切换数据源的应用。
- 希望通过分库分表提升数据库性能和扩展性的项目。

## 使用说明

1. **克隆项目**：将本项目克隆到本地。
2. **配置数据源**：根据实际需求，配置`application.yml`文件中的数据源信息。
3. **运行项目**：启动Spring Boot应用，测试动态数据源切换和分库分表功能。

## 注意事项

- 请确保已正确配置数据库连接信息。
- 分库分表规则需根据实际业务需求进行调整。

## 联系作者

如有任何问题或建议，欢迎通过博客文章评论区进行交流。

## 下载链接

[Dynamic-DatasourceShardingSphere-JDBC实现分库分表Demo](https://pan.quark.cn/s/058060f6e86a)