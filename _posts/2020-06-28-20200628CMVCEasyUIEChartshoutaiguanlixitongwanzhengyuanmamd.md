---
layout: post
title: "C MVC  EasyUI  ECharts 后台管理系统完整源码"
date:   2020-04-28
tags: [数据库,EasyUI,SQL,Server,项目]
comments: true
author: admin
---
# C# MVC + EasyUI + ECharts 后台管理系统完整源码

本仓库提供了一个基于C#的MVC架构的后台管理系统完整源码，使用了EasyUI和ECharts进行前端开发，数据库采用SQL Server 2014。该源码是在我之前上传的基础上进行了进一步的修改和功能扩展，添加了一些新功能和图形报表展示。

## 项目特点

1. **开发环境**：本项目使用Visual Studio 2012进行编译，其他版本的VS可以通过转换后使用。
2. **技术栈**：
   - 后端：C# + MVC
   - 前端：EasyUI + ECharts
   - 数据库：SQL Server 2014
3. **主要功能**：
   - 新增、修改、删除数据
   - 数据分页展示
   - 导出Excel文件
   - 图片上传功能
   - 权限设置（仅作为练习EasyUI Tree的使用，具体项目需具体分析）
   - 图形报表展示

## 数据库设计

本项目涉及两张表：
- 用户表
- 权限表

数据分页默认采用SQL Server的分页方式。

## 使用说明

1. **环境配置**：
   - 安装Visual Studio 2012或更高版本。
   - 安装SQL Server 2014或更高版本。

2. **数据库配置**：
   - 在SQL Server中创建数据库，并导入项目中提供的数据库脚本。
   - 修改项目中的数据库连接字符串，确保连接到正确的数据库。

3. **运行项目**：
   - 打开Visual Studio，加载项目。
   - 编译并运行项目，访问系统。

## 注意事项

- 权限设置功能仅作为练习EasyUI Tree的使用，具体项目中需根据实际需求进行调整。
- 本项目主要用于学习和参考，实际项目中请根据具体需求进行进一步的开发和优化。

## 贡献

欢迎大家提出问题和建议，或者提交Pull Request进行代码改进。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[CMVCEasyUIECharts后台管理系统完整源码](https://pan.quark.cn/s/b767a2c1a28c)