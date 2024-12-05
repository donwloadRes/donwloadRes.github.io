---
layout: post
title: "ASPNET WMS仓库管理系统"
date:   2024-09-08
tags: [Core,NET,仓库,数据库,ASP]
comments: true
author: admin
---
# ASP.NET WMS仓库管理系统

## 项目介绍

本仓库提供了一个基于ASP.NET Core 3.1开发的WMS（仓库管理系统）源码，适用于二次开发和定制化需求。该系统采用了.NET Core 3.1框架，结合MySQL或SQL Server数据库，以及Entity Framework Core（EF Core）进行数据访问。系统设计灵活，功能齐全，适合中小型企业或个人开发者使用。

## 主要功能

1. **用户管理**：管理系统的用户账号，包括用户注册、登录、权限分配等功能。
2. **角色管理**：定义不同角色的权限，确保系统安全性和操作规范。
3. **部门管理**：管理企业内部的部门结构，方便权限和数据的分级管理。
4. **数据字典管理**：维护系统中的数据字典，确保数据的一致性和规范性。
5. **系统日志管理**：记录系统的操作日志，便于追踪和审计。
6. **登陆统计**：统计用户的登录情况，分析用户活跃度。
7. **仓库管理**：管理仓库的基本信息，包括仓库的创建、编辑和删除。
8. **入库管理**：处理货物的入库流程，记录入库信息。
9. **出库管理**：处理货物的出库流程，记录出库信息。
10. **库存查询**：实时查询仓库中的库存情况，支持多种查询条件。
11. **发货管理**：管理货物的发货流程，确保发货的准确性和及时性。

## 技术栈

- **前端**：Vue、Polyfill、Qs、Axios、Bootstrap、AdminLTE、Layer、Bootstrap-datetimepicker、Bootstrap-table、Bootstrap-select等。
- **后端**：ASP.NET MVC Core、SqlSugar、FluentValidation、NLog、Jil、DI、Ganss、雪花算法、Xunit、NPOI等。

## 注意事项

- 本系统基于.NET Core 2.2~3.1开发，建议使用.NET Core 3.1进行部署和开发。
- 支持SQL Server和MySQL数据库，其他数据库未经过测试。数据库脚本位于`数据库sql脚本/sql`目录下。
- 前端采用了Vue等现代前端技术，确保界面友好和交互流畅。
- 后端采用了ASP.NET MVC Core等技术，确保系统的稳定性和可扩展性。
- 部分功能（如NPOI）在Linux环境下可能存在问题，已计划进行替换和修复。

## 使用说明

1. 克隆本仓库到本地。
2. 根据需要选择SQL Server或MySQL数据库，并导入相应的数据库脚本。
3. 配置数据库连接字符串。
4. 运行项目，开始使用WMS仓库管理系统。

## 贡献

欢迎开发者提交Issue和Pull Request，共同完善本项目。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[ASP.NETWMS仓库管理系统](https://pan.quark.cn/s/883e90e620c2)